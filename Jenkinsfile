pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-npm-10'
      containerTemplate {
        name 'maven'
        image 'node:10-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  environment {
    // For test.sh script benefit
    CI = 'true'
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Audit') {
      steps {
        sh 'npm audit'
      }
    }
    stage('Test') {
      steps {
        sh 'jenkins/scripts/test.sh'
      }
    }
    stage('Deliver') {
      steps {
        sh 'jenkins/scripts/deliver.sh'
      }
    }
  }
}
