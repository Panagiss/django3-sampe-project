pipeline {
    agent any


    stages {
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
