pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew :app:build'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew :app:test'
            }
        }

        stage('Run Application') {
            steps {
                sh './gradlew :app:run'
            }
        }
    }

    post {
        failure {
            echo 'Build failed!'
        }
    }
}
