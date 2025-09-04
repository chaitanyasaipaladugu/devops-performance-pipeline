pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/chaitanyasaipaladugu/devops-performance-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands, e.g., sh 'mvn clean install' for Java
            }
        }
        stage('Unit Test') {
            steps {
                echo 'Running unit tests...'
                // Add test commands, e.g., sh 'mvn test'
            }
        }
        stage('Performance Test') {
            steps {
                echo 'Running JMeter tests...'
                // Add your JMeter execution commands here
            }
        }
    }
}
