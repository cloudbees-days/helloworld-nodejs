pipeline {
  agent {label 'nodejs-app'}
  stages {
    stage('Say Hello') {
      steps {
          container('nodejs'){
          echo 'Hello World!'   
          sh 'java -version'
        }
      }
    }
  }
}
