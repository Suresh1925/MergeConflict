pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from version control
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build the Maven project
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            // This stage can be extended for deployment steps
            steps {
                // Example: Deploy to a server or push to a container registry
                echo 'Deployment steps go here'
            }
        }
    }

    post {
        success {
            // This block runs when the pipeline is successful
            echo 'Pipeline succeeded! Perform additional tasks if needed.'
        }
        failure {
            // This block runs when the pipeline fails
            echo 'Pipeline failed! Notify or take corrective actions.'
        }
    }
}
