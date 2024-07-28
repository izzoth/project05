pipeline {
    agent any

    environment {
        DOCKER_HOST = 'tcp://172.18.0.2:2375'
    }

    stages {
        stage('Install Docker Compose') {
            steps {
                script {
                    // Check if docker-compose is already installed and symlinked
                    def dockerComposeInstalled = sh(script: 'command -v docker-compose', returnStatus: true) == 0

                    if (!dockerComposeInstalled) {
                        // Download and install docker-compose
                        sh '''
                        curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
                        chmod +x /usr/local/bin/docker-compose
                        '''

                        // Create a symlink if it doesn't already exist
                        sh '''
                        if [ ! -L /usr/bin/docker-compose ]; then
                            ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
                        fi
                        '''
                    }
                }
            }
        }
        stage('Build and Run Docker Compose') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
