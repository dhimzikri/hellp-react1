pipeline {
  agent any
  tools {nodejs "NodeJS-v18.12.1"}
  stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                bat './jenkins/scripts/test.sh'
            }
        }
        // stage('Deliver') { 
        //     steps {
        //         sh './jenkins/scripts/deliver.sh' 
        //         input message: 'Finished using the web site? (Click "Proceed" to continue)' 
        //         bat './jenkins/scripts/kill.sh' 
        //     }
        // }
    }
}