pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-npm-6'
      defaultContainer 'node-container'
      yamlFile 'KubernetesPod.yaml'
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
