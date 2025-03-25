pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Prompt for manual approval before starting the build
                    input message: 'Ready to start the Build stage?', ok: 'Start Build'
                }
                echo 'Building... - 2'
                // Add your build steps here (e.g., compilation, packaging, etc.)
            }
        }
        stage('Test') {
            steps {
                script {
                    // Prompt for manual approval before running tests
                    input message: 'Proceed to the Test stage?', ok: 'Start Testing'
                }
                echo 'Testing... - 2'
                // Add your test steps here (e.g., unit tests, integration tests, etc.)
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Prompt for manual approval and let the user select the deployment environment
                    def environment = input(
                        id: 'deployInput', 
                        message: 'Approve Deployment and select the target environment:', 
                        parameters: [
                            choice(
                                name: 'Environment', 
                                choices: ['Development', 'Staging', 'Production'], 
                                description: 'Select the deployment environment'
                            )
                        ]
                    )
                    echo "Deploying to the ${environment} environment."
                }
                echo 'Deploying... - 2'
                // Add your deployment steps here (e.g., running scripts, pushing artifacts, etc.)
            }
        }
    }
}
