pipeline {
    agent {
        docker {
            image 'docker:latest'
            args '--privileged -v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Install Docker Compose') {
            steps {
                sh '''
                apk add --no-cache docker-compose
                '''
            }
        }
        stage('Start Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
