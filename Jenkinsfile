pipeline {
  agent any
  stages {
    stage ('Run Docker Compose') {
      steps{
        sh '/var/jenkins_home/workspace/Docker-Node-Project05/docker-compose up --build'
      }
    }
  }
}