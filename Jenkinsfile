pipeline {
  agent any
    environment {
      DOCKER_HOST = 'tcp://172.18.0.3:2375'
      DOCKER_CERT_PATH = '/certs/client'
      DOCKER_TLS_VERIFY = '1'  
    }
  stages {
    stage ('Run Docker Compose') {
      steps{
        sh 'docker-compose up -d'
        echo 'Docker-compose-build Build Image Completed'
      }
    }
  }
}