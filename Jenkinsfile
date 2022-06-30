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
                sh './gradlew sonarqube -Dsonar.login=6a1ea43fb933fa51756a7f29341fab961eaff194 -Dsonar.branch.name=feature-tarea-4'
            }
        }
    }
}