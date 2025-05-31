pipeline {
    agent any
    }
    environment {
        REPO_URL = 'https://github.com/yinon46/devops/pythonAPP.git'
    }
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
