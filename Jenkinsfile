pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/MakamSriyasaswini/StudentManagementArchive.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat '"C:\\Users\\makam\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
