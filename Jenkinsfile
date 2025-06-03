pipeline {
    agent any  // Run on any available agent

    environment {
        PROJECT_NAME = "my-sample-app"
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo "git-webhook session 0121319999999"
            }
        }

        stage('Build') {
            steps {
                echo "Building ${env.PROJECT_NAME}..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                 echo "Running hemanth."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    } // ← this was missing

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Investigate the logs."
        }
    }
}
