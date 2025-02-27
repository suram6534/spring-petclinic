
pipeline {
    agent any

    tools {
        gradle 'Gradle-6.8'  // Use the name you gave your Gradle installation in Jenkins' Global Tool Configuration
    }

    stages {
        stage('Clean') {
            steps {
                script {
                    // Run Gradle clean task
                    sh './gradlew clean'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run Gradle test task
                    sh './gradlew test'
                }
            }
        }

        stage('Package') {
            steps {
                script {
                    // Run Gradle build/package task
                    sh './gradlew build'  // or 'gradle assemble' depending on your project setup
                }
            }
        }
    }

    post {
        success {
            echo 'Build and tests passed successfully!'
        }
        failure {
            echo 'Build failed. Please check the logs.'
        }
    }
}
