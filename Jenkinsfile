pipeline {
  agent any
  stages {
    stage ('Run Docker Compose') {
      steps{
        sh '/var/www/html/docker-compose up -d'
      }
    }
  }
}