pipeline{
    agent any 

    stages{
        
        stage('build'){
            steps{
                echo 'Hello from Jenkins Pipeline!'
                echo 'This is the Build stage.'
            }
        }

        stage('test'){
            steps{
                 echo 'Running tests...'
            }
        }

        stage('deploy'){
            steps{
                 echo 'Deploying application...'
            }
        }
    }
}