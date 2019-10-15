pipeline {
  agent none
  stages {
    agent { label 'nodejs-app' }
    stage('Say Hello') {
      steps {
        echo 'Hello World!'   
        sh 'java -version'
      }
    }
  }
}
