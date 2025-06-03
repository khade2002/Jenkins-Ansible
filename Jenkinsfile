pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/khade2002/Jenkins-Ansible.git'
            }
        }

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
