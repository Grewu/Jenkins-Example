pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Выполнение команды Gradle для сборки проекта
                bat 'gradlew.bat build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Выполнение команды Gradle для тестирования проекта
                bat 'gradlew.bat test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Добавьте команды для деплоя вашего проекта
                bat 'echo Deploy step'
            }
        }
    }
}
