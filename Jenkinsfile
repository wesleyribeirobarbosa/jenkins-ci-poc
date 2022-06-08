pipeline {
  agent any
  stages {
    stage("run tests") {
      steps {
        sh '''
         npm install
         npm test
         '''
      }
    }
    stage("verify tooling") {
      steps {
        sh '''
          docker version
          docker info
          docker compose version 
        '''
      }
    }
    stage('Prune Docker data') {
      steps {
        sh 'docker system prune -a --volumes -f'
      }
    }
    stage('Start container') {
      steps {
        sh 'docker compose up -d --build --wait'
        sh 'docker compose ps'
      }
    }
  }
  post {
    always {
      sh 'docker system prune -a --volumes -f'
      sh 'docker compose ps'
    }
  }
}
