pipeline {
    agent any 

    stages {
        stage('Clone Repository') {
            steps {
                // Replace with your Git repository URL
                git url: 'https://github.com/GitHubDayana/TestRepo.git', branch: 'main'
            }
        }
           stage('Publish') {
            steps {
                // Restore dependencies
                sh '''
                cd TestApp
                pwd
                dotnet build
                dotnet publish -c Release -o ./var/www/Application
                '''
            }
        }
    }
}
