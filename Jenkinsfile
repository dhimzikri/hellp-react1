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
                bat 'test.sh'
            }
        }
        // stage('Deliver') { 
        //     steps {
        //         bat '/jenkins/scripts/deliver.sh' 
        //         input message: 'Finished using the web site? (Click "Proceed" to continue)' 
        //         bat '/jenkins/scripts/kill.sh' 
        //     }
        // }
    }
}