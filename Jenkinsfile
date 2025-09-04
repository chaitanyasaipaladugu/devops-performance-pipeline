pipeline {
    agent any

    environment {
        // Example: Set environment variables if needed
        JMETER_HOME = 'C:/JMeter/apache-jmeter-5.6.2'  // Update path as per your system
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code from Git...'
                git branch: 'main', url: 'https://github.com/chaitanyasaipaladugu/devops-performance-pipeline.git', credentialsId: 'git-creds'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // For Java Maven project
                // bat 'mvn clean install'
                // For Node.js project
                // bat 'npm install'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Running unit tests...'
                // For Java Maven project
                // bat 'mvn test'
                // For Node.js project
                // bat 'npm test'
            }
        }

        stage('Performance Test') {
            steps {
                echo 'Running JMeter performance tests...'
                // Example: Run JMeter test plan
                // bat "${env.JMETER_HOME}/bin/jmeter.bat -n -t testplan.jmx -l results.jtl -j jmeter.log"
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs for details.'
        }
    }
}
