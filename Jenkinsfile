pipeline {
  agent {
    kubernetes {
      def label = "mypod-${UUID.randomUUID().toString()}"
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
