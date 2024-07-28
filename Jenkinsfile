pipeline {
  agent any

  environment {
        DOCKER_HOST = 'tcp://172.18.0.2:2375'
        DOCKER_TLS_VERIFY = '1'
        DOCKER_CERT_PATH = '/certs/client'
    }  

  stages {
    stage ('Run Docker Compose') {
      steps{
        sh 'docker-compose up -d'
      }
    }
  }
}