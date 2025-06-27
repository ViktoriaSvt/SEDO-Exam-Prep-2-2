pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build'
                bat 'dotnet test'
            }
        }
    }
}
