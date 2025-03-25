pipeline {
    agent any
    stages {
        stage('Approval') {
            agent none // Do not allocate an executor here
            steps {
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
