pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ -o PES1UG22CS029-1 main/hello.cpp'
        echo 'Build Stage Successful'
      }
    }
    stage('Test'){
      steps{
        sh './PES1UG22CS029-1'
        echo 'Test Stage Successful'
        }
       post{
          always{
            junit 'target/surefire-reports/*.xml'
          }
      }
    }
    stage('Deploy'){
      steps{
        sh 'mvn deploy'
        echo 'Deployment Successful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
