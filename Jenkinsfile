pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${params.Name} from ${NODE_NAME}!"
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
        sh 'java -version'
      }
    }
    stage('Deploy') {
      input {
        message 'Should we continue?'
      }
      steps {
        echo 'Continuing with deployment'
      }
    }
  }
  environment {
    MY_NAME = 'Bhuvesh'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}