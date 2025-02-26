pipeline {
    agent any

    environment {
        GRADLE_HOME = '/usr/local/gradle'  // Adjust if Gradle is installed elsewhere
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    sh './gradlew clean build'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './gradlew test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps (e.g., deploy to AWS, Heroku, etc.)
            }
        }
    }
    post {
        success {
            echo 'Build and tests completed successfully.'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
