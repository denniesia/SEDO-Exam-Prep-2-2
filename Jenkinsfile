pipeline {
    agent any 
    stages {
        stage('Restore Dotnet Packages') { 
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') { 
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Run unit and integration Tests') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}