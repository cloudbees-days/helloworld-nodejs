pipeline {
  agent none
  stages {
    stage('Say Hello') {
      agent { label 'nodejs-app' }
      steps {
        echo 'Hello World!'
    stage('Build and Push Image') {
       when {
         beforeAgent true
         branch 'master'
       }
       steps {
        echo "TODO - build and push image"
        sh 'java -version'
       }
      }
    }
  }
}
