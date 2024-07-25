pipeline {
    agent any
    }

    stages {
        stage('Start Containers') {
            steps {
                try {
                    sh 'docker-compose up -d'
                } 
            }
        }
    }
