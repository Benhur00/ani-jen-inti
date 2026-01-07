pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Ansible Ping Test') {
            steps {
                sh '''
                ansible --version
                ansible -i hosts.ini local -m ping
                '''
            }
        }
    }
}
