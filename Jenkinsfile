pipeline {
    agent any
    stages {
        stage('Approval') {
            steps {
                script {
                    input message: 'Click "Proceed" to continue:', ok: 'Proceed'
                    echo 'Continuing with the pipeline...'
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
