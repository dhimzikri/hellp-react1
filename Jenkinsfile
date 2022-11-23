pipeline {
  agent any
  tools {nodejs "NodeJS-v18.12.1"}
  args '-p 3000:3000'
  stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm i kill-port'
            }
        }
        stage('Test') {
            steps {
                bat 'test.sh'
            }
        }
        stage('Deliver') { 
            steps {
                bat 'deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                // bat 'kill.sh' 
            }
        }
    }
}