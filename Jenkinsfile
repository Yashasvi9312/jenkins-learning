
pipeline{
    agent any

    tools{
        nodejs 'node24'
    }


    environment{
        USERNAME = 'Yash2000'
        PASSWORD = 'RandomShit12'
        SECRET_TEXT = credentials('demo-secret')
    }
    stages{

        stage('Variable Tests'){
            steps{
                bat 'echo "USERNAME : %USERNAME%"'
                bat 'echo "PASSWORD : %PASSWORD%"'
            }
        }
        stage('Dependency checks'){
            when {
                branch 'main'
            }
          steps{
            bat 'echo "Checking NodeJS"'
            bat 'node -v'
            bat 'npm -v'
          } 
        }

        stage('Dependency Installation'){
            steps{
                bat 'echo "Installing node dependencies"'
                bat 'npm install'
            }

            post{
                success{
                    echo "npm install was successfull"
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'npm run build'
            }
        }

        stage('Test') {
            when {
                branch 'test'
            }
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post{
        success{
            echo "Post Success..."
        }
        always{
            echo "Post always....."
        }
    }
}