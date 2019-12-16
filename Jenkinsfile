pipeline {
    agent {
        docker {
            image 'node:12-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {

        stage('Build') { 
            steps {
                sh './build.sh' 
            }
        }
        
        stage('Deploy') { 
            steps {
                sh './deploy.sh' 
            }
        }
    }
}