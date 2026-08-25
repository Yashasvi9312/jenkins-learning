pipeline{
    agent any 

    tools {
    nodejs 'node24'
    }
    stages{

        stage('Dependency Checks'){
          steps{
            echo 'Checking node JS...'

            bat 'node -v'
            bat 'npm -v'
            bat 'where node'
            bat 'where npm'
          }  
        }
        
        stage('build'){
            steps{
                echo 'Starting build stage......'

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