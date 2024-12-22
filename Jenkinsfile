pipeline {
    agent {
        docker { 
            image 'node:22.12.0-alpine3.21' 
        }
    }
    stages {
        stage('Check Docker') {
            steps {
                echo 'Checking Docker...'
                sh 'docker --version'
            }
        }
        stage('Test') {
            steps {
                sh 'node --eval "console.log(process.platform,process.env.CI)"'
            }
        }
    }
}
