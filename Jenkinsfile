pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Builds the C# code'
                sh "dotnet build"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}