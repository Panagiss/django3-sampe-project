pipeline {
    agent any


    stages {
        stage('Run ansible to run Django app to deployment VM') {
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
