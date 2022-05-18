pipeline {
  agent {
    node {
      label 'node_1.3'
    }

  }
  stages {
    stage('build CI stage ') {
      steps {
        sh 'mvn clean install '
      }
    }

    stage('test your jar file ') {
      steps {
        sh '''cd /home/kulkarav/.m2/repository/de/tudresden/inf/st/guestbook/1.2.0-SNAPSHOT/

java -cp guestbook-1.2.0-SNAPSHOT.jar de.tudresden.inf.st.Application'''
      }
    }

  }
}