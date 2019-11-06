pipeline {
    agent {
        docker.withTool('docker_local') {
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