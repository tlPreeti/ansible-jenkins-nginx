pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/tlPreeti/ansible-jenkins-nginx.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                sudo -u ansible ansible-playbook -i hosts install-nginx.yml
                '''
            }
        }

    }
}
