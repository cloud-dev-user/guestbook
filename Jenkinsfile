pipeline {
  agent {
    node {
      label 'node_1.3'
    }

  }
  stages {
    stage('build CI stage ') {
      steps {
        sh 'mvn clean deploy'
      }
    }

    stage('Deploy to tomcat ') {
      steps {
        sh '''cd /tmp/jardownload/
curl -L -X -O GET  "http://192.168.1.3:8099/service/rest/v1/search/assets/download?sort=version&repository=maven-snapshots&maven.groupId=de.tudresden.inf.st&maven.artifactId=guestbook&maven.extension=jar" -H "accept: application/json"
jar -cvf  guestbook.war *.jar 
cp guestbook.war /opt/tomcat/apache-tomcat-9.0.63/webapps/

cd /opt/tomcat/apache-tomcat-9.0.63/bin/ 
./catalina stop && ./catalina start '''
      }
    }

  }
}