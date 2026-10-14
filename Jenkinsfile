pipeline {
    agent any
       stages {
        stage('Checkout') {
            steps {
                echo 'Getting source code from GitHub'
                checkout scm
            }
        }
       stage('Build Docker Image') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t ayush-tutorial-app .'
            }
        }
        stage('Run Python Application') {
            steps {
                echo 'Running Python application inside Docker'
                sh 'docker run --rm ayush-tutorial-app'
            }
        }
    }
    post {
        success {
            echo 'Tutorial 5 completed successfully!'
        }
        failure {
            echo 'Tutorial 5 failed. Check the Console Output.'
        }
    }
}
