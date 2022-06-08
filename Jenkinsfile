pipeline {
  agent any
  stages {
    stage('Start container') {
      steps {
        sh 'docker-compose up --build -d'
        sh 'docker-compose ps'
      }
    }
  }
}
