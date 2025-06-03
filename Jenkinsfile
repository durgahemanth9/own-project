pipeline {
    agent any  // Run on any available agent

    environment {
        PROJECT_NAME = "my-sample-app"
    }

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/your-username/your-repo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo "Building ${env.PROJECT_NAME}..."
                // Example: Compile code, run build tools, etc.
                sh 'make build'  // or 'mvn clean package' if using Maven
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Run unit tests or integration tests
                sh 'make test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Example deployment step (replace with your own)
                sh './scripts/deploy.sh'
            }
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
