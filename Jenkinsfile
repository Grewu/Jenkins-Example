pipeline {
    agent any
    triggers {
        pollSCM('H/5 * * * *') // Проверка каждые 5 минут
    }

    stages {
        stage('Pull Request Validation') {
            when {
                expression {
                    // Проверяем, что это  целевая ветка — main
                    return env.TARGET_BRANCH == 'main'
                }
            }
            steps {
                echo "Validating PR #${env.CHANGE_ID} from branch ${env.CHANGE_BRANCH} targeting ${env.TARGET_BRANCH}"
                // Выполнение сборки проекта
                bat 'gradlew.bat build'
                // Выполнение тестов проекта
                bat 'gradlew.bat test'
            }
        }
    }
}
