pipeline {
  agent { label 'nodejs-app' }
  stages {
    stage('Test') {
      steps {
        sh 'java -version'
        container('nodejs') {
          echo 'Hello!'   
          sh 'node --version'
        }
      }
    }
  }
}
