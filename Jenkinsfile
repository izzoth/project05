pipeline {
    agent any

    environment {
        DOCKER_TLS_VERIFY = '1'
        DOCKER_HOST = 'tcp://docker:2376'
        DOCKER_CERT_PATH = '/certs/client'
    }

    stages {
        stage('Deploy') {
            steps {
                script {
                    // Run the Docker containers
                    sh 'sudo docker-compose up -d'
                }
            }
        }
    }
}
