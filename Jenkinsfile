pipeline {
    agent any
    
  environment {
		NODE_HOME="${tool 'nodejs'}"
        PATH="${env.NODE_HOME}/bin:${env.PATH}"
	}
    
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