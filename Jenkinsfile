pipeline {
    agent any

    stages {
        stage('Pull Request Validation') {
            when {
                expression {
                    // Проверяем, что это PR и целевая ветка — main
                    return env.CHANGE_ID != null && env.TARGET_BRANCH == 'main'
                }
            }
            steps {
                echo "Validating PR #${env.CHANGE_ID} from branch ${env.CHANGE_BRANCH} targeting ${env.TARGET_BRANCH}"
                bat 'gradlew.bat build'
                bat 'gradlew.bat test'
            }
        }
    }
}
