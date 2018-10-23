def label = "mypod-${UUID.randomUUID().toString()}"

pipeline {
  agent {
    kubernetes {
      label label
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
