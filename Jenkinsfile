pipeline {
//    agent {
//      label 'docker_local' 
//    }
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
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}