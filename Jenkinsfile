pipeline {
    agent any
    }

    stages {
        stage('Build Images') {
            when {
                expression { params.rebuild }
            }
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Start Containers') {
            steps {
                try {
                    sh 'docker-compose up -d'
                } catch (err) {
                    echo 'Error starting containers: ${err.message}'
                    error 'Container startup failed'
                }
            }
        }
    }
}
