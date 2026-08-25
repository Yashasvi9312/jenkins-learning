pipeline{
    agent any 

    stages{
        
        stage('build'){
            steps{
                echo 'Starting build stage...'

                bat 'echo Hello from Windows!'
                bat 'dir'
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