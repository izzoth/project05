pipeline {
    agent {
        docker {
            image 'docker/compose:1.29.2'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    environment {
        DOCKER_HOST = 'tcp://172.18.0.2:2375'
    }
    stages {
        stage('Start Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
