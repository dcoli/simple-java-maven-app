pipeline {
    agent {
      label 'docker_local' 
    }
    stages {
        stage('Build') { 
            agent {
                docker {
                    // Set both label and image
                    label 'docker_local'
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