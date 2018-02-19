pipeline {
  agent {
    node {
      label 'java7'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        echo 'Building Stage'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing Stage'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying Stage'
      }
    }
  }
}