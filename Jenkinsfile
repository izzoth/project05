pipeline {
  agent any

  environment {
        DOCKER_HOST = 'tcp://docker:2376'
    }  

  stages {
    stage ('Run Docker Compose') {
      steps{
        sh 'docker-compose up -d'
      }
    }
  }
}