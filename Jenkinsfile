pipeline {
    agent any

    stages {
        stage('Check Gradle Version') {
            steps {
                echo 'Checking Gradle version...'
                sh 'gradle --version'
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
                sh 'echo Deploy step'
            }
        }
    }
}
