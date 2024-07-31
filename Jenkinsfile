pipeline {
    agent any
    environment {
        DOCKER_TLS_VERIFY = '1'
        DOCKER_CERT_PATH = '/certs/client'
	    DOCKER_HOST = 'unix:///var/run/docker.sock'
    }
    stages {
        stage('Build') {
            steps {
                        // Example of a Docker command
                        sh 'docker-compose up -d'
                    }
                }
            }
        }
        
