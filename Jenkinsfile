pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG22CS029-1 main/hello.cpp'  // Ensure correct path
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG22CS029-1'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
