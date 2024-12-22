pipeline {
    agent {
        docker {
            image 'gradle:7.3.3-jdk11'
            args '-v /var/jenkins_home/workspace:/workspace'
        }
    }

    stages {
        stage('Check Docker') {
            steps {
                echo 'Checking Docker...'
                sh 'docker --version'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'gradle build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'gradle test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Добавьте команды для деплоя вашего приложения
            }
        }
    }
}
