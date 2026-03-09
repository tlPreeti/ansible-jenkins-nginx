pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/username/ansible-jenkins-nginx.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                sudo su - ansible -c "ansible-playbook -i hosts install-nginx.yml"
                '''
            }
        }

    }
}