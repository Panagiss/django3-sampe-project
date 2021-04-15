pipeline {
    agent any


    stages {
        stage('Run ansible playbook for Django') {
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
