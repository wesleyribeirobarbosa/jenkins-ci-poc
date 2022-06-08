pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh '''
          docker version
          docker info
          docker compose version 
        '''
      }
    }
    stage('Start container') {
      steps {
        sh 'docker compose up -d --build --wait'
        sh 'docker compose ps'
      }
    }
  }
}
