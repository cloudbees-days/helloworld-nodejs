pipeline {
  agent none
  stages {
    stage('Say Hello') {
      agent { label 'nodejs-app' }
      steps {
        echo 'Hello There!'   
        sh 'java -version'
      }
    }
  }
}
