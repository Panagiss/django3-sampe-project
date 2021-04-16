pipeline {
    agent any


    stages {
        stage('Install Postgres for Django App') {
            steps {
                sh '''
                    cd ~/workspace/ansible-project/
                    echo $WORKSPACE
                    ansible-playbook playbooks/postgres.yml
                '''
            }
        }
        stage('Ansible job to install and run Django app to deployment VM') {
            steps {
                sh '''
                    cd ~/workspace/ansible-project/
                    echo $WORKSPACE
                    ansible-playbook playbooks/django-project-install.yml
                '''
            }
        }
    }
}
