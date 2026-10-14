pipeline {
    agent any
  stages {
        stage('Coding') {
            steps {
                echo 'Checking Python version'
                sh 'python3 --version'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing the application'
            }
        }
        stage('Deployment') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
