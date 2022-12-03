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
//         stage('Test') {
//             steps {
//                 sh 'npm test'
//             }
//         }
        stage('Deliver') { 
            steps {
                sh 'npm start & sleep 1' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                // bat 'kill.sh' 
            }
        }
    }
}
