pipeline {
  agent any
  stages {
    stage("unit testing") {
      steps {
        sh '''
          npm i
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
    stage("build") {
      steps {
        sh '''
          docker-compose up --build --force-recreate -d
          sh 'docker-compose ps'
        '''
      }
    }
  }
}

