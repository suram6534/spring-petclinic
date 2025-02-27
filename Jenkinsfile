
pipeline {
    agent any

    tools {
        maven 'Maven 3'  // Name defined in Global Tool Configuration
    }

    stages {
        stage('Build') {
            steps {
                // Running Maven commands
                sh 'mvn clean install'  // Run Maven clean install
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'  // Run Maven tests
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'  // Run Maven package
            }
        }
    }
}

