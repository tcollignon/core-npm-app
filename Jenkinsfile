pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-npm-6'
      containerTemplate {
        name 'maven'
        image 'node:6-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}
