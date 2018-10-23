pipeline {
  agent {
    kubernetes {
      label "mypod-${UUID.randomUUID().toString()}"
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
