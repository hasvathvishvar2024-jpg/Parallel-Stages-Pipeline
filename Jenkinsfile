pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'YOUR_PROJECT_3_GITHUB_URL'
            }
        }

        stage('Parallel Checks') {
            parallel {
                stage('Frontend Check') {
                    steps {
                        bat 'C:/Users/ASUS/AppData/Local/Programs/Python/Python313/python.exe frontend.py'
                    }
                }

                stage('Backend Check') {
                    steps {
                        bat 'C:/Users/ASUS/AppData/Local/Programs/Python/Python313/python.exe backend.py'
                    }
                }
            }
        }

        stage('Complete') {
            steps {
                echo 'Frontend and Backend checks completed successfully.'
            }
        }
    }
}