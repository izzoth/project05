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
                script {
                    docker.image('docker:latest').inside('--privileged -v /var/run/docker.sock:/var/run/docker.sock') {
                        // Example of a Docker command
                        sh 'sudo docker --version'
                    }
                }
            }
        }
        
    }
}
