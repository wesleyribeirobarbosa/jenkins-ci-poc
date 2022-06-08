pipeline {
  agent any
  stages {
    stage('Start container') {
      steps {
        sh 'docker compose up'
        sh 'docker compose ps'
      }
    }
  }
}
