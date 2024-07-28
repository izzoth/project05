pipeline {
    agent any

    stages {
        stage('Install Docker Compose') {
            steps {
                sh 'curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose'
                sh 'chmod +x /usr/local/bin/docker-compose'
                sh 'ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose'
            }
        }
        stage('Build and Run Docker Compose') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
