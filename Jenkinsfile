pipeline {
    agent any

    stages {
        // Stage for building the application
        stage('Build') {
            steps {
                echo 'Building Java application'
                // You can add build commands here, e.g., running Maven or Gradle commands
                // sh 'mvn clean install'  // For Maven build example
            }
        }

        // Stage for testing the application
        stage('Test') {
            steps {
                echo 'Running tests'
                // You can add test commands here, for example running unit tests
                // sh 'mvn test'  // For Maven test example
            }
        }

        // Stage for deploying the application
        stage('Deploy') {
            steps {
                echo 'Deploying the application'
                // Add deployment steps here, e.g., using SSH to deploy to a server
                // sh './deploy.sh'  // Example deploy script
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed'
        }
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
