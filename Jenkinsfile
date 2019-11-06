pipeline {
    agent { label 'any' }
    stages {
        stage('Build') { 
            agent {
                docker {
                    // Set both label and image
                    label 'any'
                    image 'maven:3-alpine' 
                    args '-v /root/.m2:/root/.m2'
		}
            }
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}