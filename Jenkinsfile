pipeline {
  agent none
  stages {
    stage('Test'){
      agent{ label 'nodejs-app'}
    stage('say Hello'){
      steps {
        container('nodejs')
        echo 'Hello World!'
        sh 'java -version'
      } 
     }
    }
  } 
}
