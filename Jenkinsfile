pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/hasvathvishvar2024-jpg/Parallel-Stages-Pipeline.git'
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