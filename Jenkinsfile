pipeline {
  agent any
  tools {nodejs "NodeJS-v18.12.1"}
  stages {
    stage('Build') {
      steps {
        // git 'https://github.com/dhimzikri/hellp-react1.git'
        // echo 'Installing node_modules'
        bat 'npm install'
      }
    }
    stage('Test') { 
            steps {
                sh 'test.sh'
            }
        }
  }
}