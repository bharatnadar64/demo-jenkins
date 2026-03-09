pipeline {
    agent any
    stages {
        stage('Fetching File') {
            steps {
                // Fixed: Changed curly quotes to straight quotes
                git url: 'https://github.com/bharatnadar64/demo-jenkins'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Project'
                bat 'javac Hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing Program'
                bat 'java Hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
