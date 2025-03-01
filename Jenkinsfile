pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/NixScotch/ci-cd-demo.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Install dependencies globally (no virtual environment) using Windows Command Prompt
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                // Run tests using pytest via Command Prompt
                bat 'pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Flask app...'
                // Add your deployment commands here if needed
            }
        }
    }
}
