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
                sh 'pwd'
            }
        }
    }
}
