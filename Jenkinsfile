pipeline {
    agent any
    tools {
        jdk 'jdk21' 
    }
    stages {
        stage('Build & Test') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew clean build'
            }
        }
        stage('Custom Output') {
            steps {
                sh './gradlew display'
            }
        }
    }
    post {
        success { echo 'All passed!' }
    }
}
