pipeline {
    agent any

    stages {
        stage('Install Requirements') {
            steps {
                sh '''
                    python3 -m venv venv
                    source venv/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Deploy Locally via Ansible') {
            steps {
                sh '''
                    source venv/bin/activate
                    ansible-playbook deploy.yml
                '''
            }
        }
    }
}
