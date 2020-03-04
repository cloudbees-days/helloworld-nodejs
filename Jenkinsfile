pipeline {
  agent none 
  options {
    buildDescarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Test') {
      agent { label 'nodejs-app' }
      steps {
         checkout scm
         container('nodejs') {
          echo 'Hello World!'
          sh 'node --version'
      }
    }
   }
  }
}
