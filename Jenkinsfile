pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        node {
          label 'java7'
        }
        
      }
      steps {
        echo 'Building Stage'
        stash(name: 'Java 8', includes: 'target/**')
      }
    }
    stage('Test') {
      agent {
        node {
          label 'java7'
        }
        
      }
      steps {
        unstash 'Java 8'
        echo 'Testing Stage'
      }
    }
    stage('Deploy') {
      agent {
        node {
          label 'java7'
        }
        
      }
      steps {
        unstash 'Java 8'
        echo 'Deploying Stage'
      }
    }
  }
}