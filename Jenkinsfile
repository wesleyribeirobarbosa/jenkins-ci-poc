pipeline {
  agent any
  stages {
    stage('Start container') {
      steps {
        sh 'docker compose up -d --build --wait'
        sh 'docker compose ps'
      }
    }
  }
}
