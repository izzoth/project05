pipeline {
    agent any

    environment {
        DOCKER_TLS_VERIFY = '1'
        DOCKER_HOST = 'tcp://docker:2376'
        DOCKER_CERT_PATH = '/certs/client'
    }

    stages {
       stage('Build') {
            steps {
                script {
                    // Build the Docker images
                    sh 'docker-compose build'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Run the Docker containers
                    sh 'docker-compose up -d'
                }
            }
        }
    }

    post {
        always {
            // Clean up actions, if necessary
            script {
                sh 'docker-compose down'
            }
        }
    }
}
