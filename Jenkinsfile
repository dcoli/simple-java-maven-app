pipeline {
//    agent {
//      label 'docker' 
//    }
            agent {
                docker_local.withTool('') {
                    // Set both label and image
//                    label 'docker'
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