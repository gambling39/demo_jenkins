pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system (e.g., Git)
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/gambling39/demo_jenkins.git']]])
            }
        }

        stage('Build') {
            steps {
                // Use a tool such as Maven or Gradle to build the Spring Boot project
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests, if applicable
                bat 'mvn test'
            }
        }

    }
}