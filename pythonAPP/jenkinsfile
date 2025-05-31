pipeline {
    agent any
    stages {
        stage('Welcome') {
            steps {
                echo 'Welcome to Jenkins Python CI!'
            }
        }
        stage('Install Python & Check Version') {
            steps {
                sh 'python --version'
            }
        }
        stage('Run app') {
            steps {
                sh 'python3 calculator.py'
            }
        }
        stage('Run Unit Tests') {
            steps {
                sh 'python3 test_calculator.py'
            }
        }
    }
}
