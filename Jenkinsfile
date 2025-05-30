pipeline {
    agent {
        docker {
            image 'python:3.10'   // בוחר image עם Python מותקן מראש
            args '-u root:root'   // רץ כ-root אם צריך הרשאות (לא חובה)
        }
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'cd pythonAPP && python3 test.py'
            }
        }
    }
}
