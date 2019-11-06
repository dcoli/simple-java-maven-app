pipeline {
    agent { label 'dockerlocal' }
    stages {
        stage('Build') { 
    agent {
      docker {
           image 'maven:3-alpine'
           args '--privileged -v /root/.m2:/root/.m2'
      }
    }
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}