pipeline {
    agent none
    environment {
        DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
    }
    stages {
        stage('Dotnet Build and Test') {
            agent {
                docker { 
                    image 'mcr.microsoft.com/dotnet/sdk:3.1' 
                    args '-u root:root'
                }
            }
            steps {
                sh 'dotnet build'
                sh 'dotnet test'
            }
        }
        stage('Test') {
            agent any
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            agent any
            steps {
                echo 'Deploying....'
            }
        }
    }
}