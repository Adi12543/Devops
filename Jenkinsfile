pipeline {
    agent any

    stages {
        stage('Deploy to XAMPP') {
            steps {
                bat 'xcopy /E /Y .\\*.html "C:\\xampp\\htdocs\\"'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
