pipeline {
  agent any
  tools {nodejs "NodeJS"}
  stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm i kill-port'
            }
        }
        stage('Test') {
            steps {
                sh 'test.sh'
            }
        }
        stage('Deliver') { 
            steps {
                sh 'deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                // bat 'kill.sh' 
            }
        }
    }
}
