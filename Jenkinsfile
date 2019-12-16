pipeline {
  agent none
  stages {
    stage('Test') {
      agent { label 'mcphej-nodejs-app' }
      steps {
        container('nodejs') {
        echo 'Hello World!'   
        sh 'java -version'
       }
      }
    }
  }
}
