pipeline {
  agent {
    node {
      label 'node_1.3'
    }

  }
  stages {
    stage('build CI stage ') {
      steps {
        sh '''java -version
javac -version 
./mvnw clean package'''
      }
    }

  }
}