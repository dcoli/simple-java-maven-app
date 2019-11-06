pipeline {
            agent {
                docker {
                    // Set both label and image
                    // label 'docker_local'
                    image 'maven:3-alpine' 
                    args '-v /root/.m2:/root/.m2'
		}
            }
    stages {
        stage('Build') { 
            steps {
                sh 'export PATH=$PATH:/usr/local/bin; mvn -B -DskipTests clean package'
            }
        }
    }
}