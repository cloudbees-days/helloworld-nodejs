pipeline {
  agent {label 'nodejs-app'}
  stages {
    stage('Say Hello') {
      steps {
        sh 'java -version'
          container('nodejs'){
          echo 'Hello World!'   
          sh 'java -version'
        }
      }
    }
  }
}
