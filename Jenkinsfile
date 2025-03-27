pipeline {
    agent any
    stages {
        stage('User Input URL') {
            steps {
                script {
                    def userUrl = input(
                        id: 'urlInput', message: 'Enter the URL to proceed:', parameters: [
                            string(defaultValue: 'http://example.com', description: 'Provide a URL', name: 'URL')
                        ]
                    )
                    echo "User entered URL: ${userUrl}"
                }
            }
        }

        stage('Use URL') {
            steps {
                echo 'This stage runs after user input.'
                // You can use the URL here if needed
            }
        }
    }
}
