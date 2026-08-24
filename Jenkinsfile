pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
                echo 'This is my Build stage.'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}