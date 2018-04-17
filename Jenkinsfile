pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello ${MY_NAME}!'
        sh 'go version'
      }
    }
  }
  environment {
    MY_NAME = 'Bhuvesh'
  }
}