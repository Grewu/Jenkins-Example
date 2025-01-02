pipeline {
    agent any
    triggers {
      // cron('H/5 * * * *')  Проверка каждые 5 минут
    }

    stages {
        stage('Pull Request Validation') {
            steps {
                // Выполнение сборки проекта
                bat 'gradlew.bat build'
                // Выполнение тестов проекта
                bat 'gradlew.bat test'
            }
        }
    }
}
