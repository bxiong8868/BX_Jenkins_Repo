pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building Stage'
        echo '$BUZZ_NAME'
      }
    }
    stage('Publish JUnit Test results report') {
      steps {
        echo 'Testing Stage result'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying Stage'
      }
    }
  }
  environment {
    BUZZ_NAME = 'Worker Bee'
  }
}