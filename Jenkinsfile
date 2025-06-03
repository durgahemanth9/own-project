pipeline {
    agent any  // Run on any available agent

    environment {
        PROJECT_NAME = "my-sample-app"
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo "git-webhook session 01213123"
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
               
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Investigate the logs."
        }
    }
}
