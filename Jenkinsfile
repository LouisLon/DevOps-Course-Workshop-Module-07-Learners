pipeline {
    agent none
    stages {
        stage('Dotnet Build') {
            agent {
                docker { 
                    image 'mcr.microsoft.com/dotnet/sdk:3.1' 
                    args '-u root:root'
                }
            }
            steps {
                sh 'dotnet build' 
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