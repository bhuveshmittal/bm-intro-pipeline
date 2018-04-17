pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${MY_NAME}"
        sh 'java -version'
      }
    }
    stage('Get Kernel') {
      steps {
        script {
          try {
            KERNEL_VERSION = sh (script: "uname -r", returnStdout: true)
          } catch(err) {
            echo "CAUGHT ERROR: ${err}"
            throw err
          }
        }
        
      }
    }
    stage('Say Kernel') {
      steps {
        echo "${KERNEL_VERSION}"
      }
    }
  }
  environment {
    MY_NAME = 'Bhuvesh'
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
}