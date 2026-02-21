pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                expression {
                    return env.GIT_BRANCH == 'origin/main'
                }
            }
            steps {
                echo 'Building...'
                bat 'dotnet build'
            }
        }
        stage('Test') {
            when {
                expression {
                    return env.GIT_BRANCH == 'origin/main'
                }
            }
            steps {
                echo 'Testing...'
                bat 'dotnet test'
            }
        }
    }
}