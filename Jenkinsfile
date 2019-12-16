pipeline {
  agent none
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
  }
  stages {
    stage('Test') {
      agent {
        kubernetes {
          label 'nodejs-app-pod'
          yamlFile 'nodejs-pod.yaml'
        }
      }
    }
    }
    stage('Build and Push Image') {
      when {
         beforeAgent true
         branch 'master'
      }
      steps {
         echo "TODO - build and push image"
      }
    }
  }
}
