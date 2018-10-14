pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-npm-6'
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
  }
}
