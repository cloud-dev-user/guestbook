pipeline {
  agent {
    node {
      label 'node_1.3'
    }

  }
  stages {
    stage('build CI stage ') {
      steps {
        sh '''mvn org.apache.maven.plugins:maven-release-plugin:3.0.0-M5:perform -DconnectionUrl=scm:git:https://github.com/cloud-dev-user/guestbook/tree/feature/cicd
mvn clean release:perform'''
      }
    }

  }
}