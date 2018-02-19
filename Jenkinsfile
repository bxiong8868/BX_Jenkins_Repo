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
    stage('Confirm Deploy') {
      steps {
        input(message: 'Okay to Deploy to Staging?', ok: 'Let\'s Do it!')
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
}