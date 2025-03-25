pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                script {
                    def deployEnv = input(
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
                    echo "Deploying to the ${deployEnv} environment."
                }
                // Place your deployment steps here.
            }
        }
    }
}
