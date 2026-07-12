pipeline {
    agent any

    tools {
        maven 'MAVEN00'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Nouvelle version du pipeline'
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Pipeline terminé avec succès.'
        }
        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}