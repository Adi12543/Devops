pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                git 'https://github.com/Aditi12543/Devops.git'
            }
        }

        stage('Deploy') {
            steps {
                // Copy HTML files to Xampp htdocs directory
                sh 'cp *.html /opt/lampp/htdocs/'
            }
        }
    }
}
