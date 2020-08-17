pipeline {
    agent any
    
    tools {nodejs "node"}
    
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