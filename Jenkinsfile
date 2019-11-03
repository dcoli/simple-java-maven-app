pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '--privileged -v /root/.m2:/root/.m2' 
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