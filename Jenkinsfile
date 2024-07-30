pipeline {
    agent any {
	docker {
            image 'docker:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    environment {
        DOCKER_TLS_VERIFY = '1'
        DOCKER_CERT_PATH = '/certs/client'
	    DOCKER_HOST = 'unix:///var/run/docker.sock'
    }

    stages {
        stage('Deploy') {
            steps {
                script {
                    // Run the Docker containers
                    sh 'docker-compose up -d'
                }
            }
        }
    }
  }
}
