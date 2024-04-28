pipeline {
    agent any
    
    environment {
        XAMPP_PATH = 'YOUR_XAMPP_PATH' // Provide the path to your XAMPP htdocs directory
    }
    
    stages {
        stage('Clone repository') {
            steps {
                script {
                    // Clone the GitHub repository
                    git branch: 'master', url: 'https://github.com/Adi12543/Devops.git'
                }
            }
        }
        
        stage('Deploy to XAMPP server') {
            steps {
                // Copy HTML files to XAMPP htdocs directory
                bat "xcopy /s /y index.html \"${env.XAMPP_PATH}\""
                bat "xcopy /s /y about.html \"${env.XAMPP_PATH}\""
                bat "xcopy /s /y contact.html \"${env.XAMPP_PATH}\""
            }
        }
    }
}


