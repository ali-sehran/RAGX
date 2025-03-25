pipeline {
    agent any
    stages {
        stage('Approval') {
            steps {
                script {
                    def userInput = input message: 'Click "Proceed" to continue:', ok: 'Proceed'
                    echo "Response recorded: User selected '${userInput}'"
                }
            }
        }
        stage('Next Stage') {
            steps {
                echo 'This stage runs after the approval.'
            }
        }
    }
}
