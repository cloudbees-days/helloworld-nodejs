pipeline {
    agent { label 'nodejs-app' }
    options {
        buildDiscarder(logRotator(numToKeepStr: '2'))
            skipDefaultCheckout true
    }
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
