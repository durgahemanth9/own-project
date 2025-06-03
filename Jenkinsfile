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
        stage('Build') {
            when {
                expression {
                    params.START_STAGE == 'All' || params.START_STAGE == 'Build'
                }
            }
            steps {
                echo "Running Build Stage"
                sh "git branch: 'main', url: 'https://github.com/durgahemanth9/own-project.git' "
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
