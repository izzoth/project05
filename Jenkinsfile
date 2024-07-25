pipeline {
    agent any

    stages {
        stage('Build') {
            when {
                branch 'main' // Optional: Only build on master branch
            }
            steps {
                // Add build steps if needed (e.g., npm install, maven build)
            }
        }

        stage('Start Containers') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}