pipeline {
  agent none
  stages {
    stage('Test') {
      agent { label 'nodejs-app' }
      steps {
        echo 'Hello World!'
        sh 'java -version'
      }
    }
  }
}
