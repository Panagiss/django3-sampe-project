pipeline {
    agent any


    stages {
        stage('Install Postgres Role with Ansible Galaxy') {
            steps {
                sh '''
                    ansible-galaxy install geerlingguy.postgresql
                '''
            }
        }
        stage('Install Postgres for Django App') {
            steps {
                sh '''
                    cd ~/workspace/ansible-project/
                    echo $WORKSPACE
                    pwd
                    ansible-playbook playbooks/postgres.yml
                '''
            }
        }
        stage('Ansible job to install and run Django app to deployment VM') {
            steps {
                sh '''
                    cd ~/workspace/ansible-project/
                    echo $WORKSPACE
                    pwd
                    ansible-playbook playbooks/django-project-install.yml
                '''
            }
        }
    }
}
