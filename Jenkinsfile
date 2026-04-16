pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/stutimahesh/MyGradleApp.git'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x gradlew'
                sh 'bash ./gradlew :app:build'
            }
        }

        stage('Test') {
            steps {
                sh 'bash ./gradlew :app:test'
            }
        }

        stage('Run Application') {
            steps {
                sh 'bash ./gradlew :app:run'
            }
        }
    }

    post {
        failure {
            echo 'Build failed!'
        }
    }
}
