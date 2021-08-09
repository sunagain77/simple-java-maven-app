pipeline {
	agent any
    stages {
        stage('Build') {
            steps {
            	bat 'd:'
            	bat 'cd C:\Users\gengxue\.jenkins\workspace\simple-java-maven-app'
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        
    }
}
