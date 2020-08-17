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
		nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
                    sh 'npm config ls'
		}
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