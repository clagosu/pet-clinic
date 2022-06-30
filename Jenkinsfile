pipeline {
    agent any 
    stages {
        stage('SCM') {
            steps {
                checkout scm 
            }
        }

        stage('SAST') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew sonarqube'
            }
        }
    }
}