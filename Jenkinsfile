pipeline {
            agent {
              docker {
                image 'maven:3-alpine'
                args '--privileged -v .m2:.m2'
              }
            }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}