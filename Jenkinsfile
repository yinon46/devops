pipeline {
    agent {
        docker {
            image 'python:3.10'
        }
    }
    environment {
        REPO_URL = 'https://github.com/yinon46/devops.git'
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
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: "${REPO_URL}"
            }
        }
        stage('Run Unit Tests') {
            steps {
                sh 'python -m unittest discover .'
            }
        }
    }
    post {
        always {
            mail to: 'yinon46levi@gmail.com',
                 subject: "Build ${currentBuild.currentResult}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                 body: "Check Jenkins for details: ${env.BUILD_URL}"
        }
    }
}
