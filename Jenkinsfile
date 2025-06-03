pipeline {
    agent any

    parameters {
        choice(
            name: 'START_STAGE',
            choices: ['All', 'Build', 'Test', 'Deploy'],
            description: 'Stage to start from'
        )
    }

    stages {
        stage('Checkout SCM') {
            when {
                expression {
                    params.START_STAGE == 'All' || params.START_STAGE == 'Build'
                }
            }
            steps {
                git branch: 'main', url: 'https://github.com/amarss321/End-to-End-Devops-WorkShop.git'
            }
        }

        stage('Build') {
            when {
                expression {
                    params.START_STAGE == 'All' || params.START_STAGE == 'Build'
                }
            }
            steps {
                echo "Running Build Stage"
            }
        }

        stage('Test') {
            when {
                expression {
                    params.START_STAGE == 'All' || params.START_STAGE == 'Test'
                }
            }
            steps {
                echo "Running Test Stage"
            }
        }

        stage('Deploy') {
            when {
                expression {
                    params.START_STAGE == 'All' || params.START_STAGE == 'Deploy'
                }
            }
            steps {
                echo "Running Deploy Stage"
            }
        }
    }
}
