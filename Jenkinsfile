pipeline {
    agent {
        docker {
            image 'docker/compose:1.29.2'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Start Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
