pipeline {
  agent any
  stages {
    stage ('Run Docker Compose') {
      steps{
        sh '/usr/local/bin/docker-compose up --build'
      }
    }
  }
}