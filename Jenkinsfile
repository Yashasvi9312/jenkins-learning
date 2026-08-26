// pipeline{
//     agent any 

//     tools {
//     nodejs 'node24'
//     }
//     stages{

//         stage('Dependency Checks'){
//           steps{
//             echo 'Checking node JS...'

//             bat 'node -v'
//             bat 'npm -v'
//             bat 'where node'
//             bat 'where npm'
//           }  
//         }
        
//         stage('build'){
//             steps{
//                 echo 'Starting build stage......'

//                 bat 'echo Hello from Windows!'
//                 bat 'dir'
//             }
//         }

//         stage('test'){
//             steps{
//                  echo 'Running tests...'
//             }
//         }

//         stage('deploy'){
//             steps{
//                  echo 'Deploying application...'
//             }
//         }
//     }
// }


pipeline{
    agent any

    tools{
        nodejs 'node24'
    }

    stages{
        stage('Dependency checks'){
          step{
            bat 'echo "Checking NodeJS"'
            bat 'node -v'
            bat 'npm -v'
          } 
        }

        stage('Dependency Installation'){
            step{
                bat 'echo "Installing node dependencies"'
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'npm run build'
            }
        }

        stage('Test') {
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
}