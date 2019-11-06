pipeline {
    agent { label 'any' }
    stages {
        stage('Build') { 
            agent {
                docker {
                    label 'any'
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