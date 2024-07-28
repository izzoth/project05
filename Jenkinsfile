pipeline {
  agent any

  environment {
        DOCKER_HOST = 'tcp://localhost:2376'
    }  

  stages {
    stage ('Run Docker Compose') {
      steps{
        sh 'docker-compose up -d'
      }
    }
  }
}