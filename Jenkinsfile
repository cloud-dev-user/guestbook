pipeline {
  agent {
    node {
      label 'node_1.3'
    }

  }
  stages {
    stage('build CI stage ') {
      steps {
        sh 'mvn clean package'
      }
    }

  }
}