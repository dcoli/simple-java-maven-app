pipeline {
    agent { label 'dockerserver' }
    stages {
        stage('Build') { 
            agent {
                docker {
                    label 'dockerserver'
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