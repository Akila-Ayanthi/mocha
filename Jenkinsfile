pipeline {
    agent any
    
  
    
    stages {
        stage('Cloning Git') {
            steps {
                git 'https://github.com/Akila-Ayanthi/mocha'
            }
        }
        stage('Install Dependencies'){
            steps {
                sh 'npm install'
            }
        }
        stage ('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}