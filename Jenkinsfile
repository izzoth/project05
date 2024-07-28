pipeline {
  agent any

  environment {
        DOCKER_HOST = 'tcp://172.18.0.2:2375'
    }  

  stages {
    stage ('Run Docker Compose') {
      steps{
        sh 'docker-compose up -d'
      }
    }
  }
}