pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building Stage'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing Stage'
          }
        }
        stage('Publish JUnit Test results report') {
          steps {
            echo 'Testing Stage result'
            junit '**/surefire-reports/**/*.xml'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying Stage'
      }
    }
  }
}