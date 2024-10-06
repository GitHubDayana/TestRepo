pipeline {
    agent any 

    stages {
        stage('Clone Repository') {
            steps {
                // Replace with your Git repository URL
                git url: 'https://github.com/GitHubDayana/TestRepo.git', branch: 'main'
            }
        }
           stage('Restore Dependencies') {
            steps {
                // Restore dependencies
                sh 'dotnet restore'
            }
        }

        stage('Build') {
            steps {
                // Build the application
                sh 'dotnet build'
            }
        }

        stage('Test') {
            steps {
                // Run unit tests
                sh 'dotnet test'
            }
        }

        stage('Publish') {
            steps {
                // Publish the application
                sh 'dotnet publish -c Release -o ./var/www/Application'
            }
        }
    }
}
