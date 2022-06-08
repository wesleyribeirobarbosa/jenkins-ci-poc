pipeline {
  agent any
  stages {
    stage("verify tooling") {
     steps {
        sh '''
          npm i
          npm test
        '''
      }
      steps {
        sh '''
          docker version
        '''
      }
    }
  }
}
