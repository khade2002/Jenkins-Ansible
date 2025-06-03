pipeline {
    agent any

    stages {
        stage('Install Requirements') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Deploy Locally via Ansible') {
            steps {
                sh 'ansible-playbook deploy.yml'
            }
        }
    }
}
