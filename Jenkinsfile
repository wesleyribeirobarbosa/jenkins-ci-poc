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
        '''
      }
    }
  }
}
