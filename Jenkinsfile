pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Prince000003/prince-the-hero.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful'
                bat 'dir'
            }
        }

        stage('Deploy to XAMPP') {
            steps {
                bat '''
                rmdir /S /Q C:\\xampp\\htdocs\\princehero
                mkdir C:\\xampp\\htdocs\\myproject
                xcopy /E /I /Y * C:\\xampp\\htdocs\\myproject
                '''
            }
        }
    }
}