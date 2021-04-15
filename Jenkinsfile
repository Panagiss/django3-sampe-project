pipeline {
    agent any


    stages {
        stage('Run ansible playbook for Django') {
            steps {
                sh '''
                    cd ~/workspace/ansible-project/
                    ansible-playbook playbooks/django-project-install.yml
                '''
            }
        }
    }
}
