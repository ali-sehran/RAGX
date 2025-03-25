pipeline {
    agent any
    stages {
        stage('Approval') {
            steps {
                // This input step will pause the pipeline and display a "Proceed" button.
                input message: 'Click "Proceed" to continue:', ok: 'Proceed'
                echo 'Continuing with the pipeline...'
            }
        }
        stage('Next Stage') {
            steps {
                echo 'This stage runs after the approval.'
            }
        }
    }
}
