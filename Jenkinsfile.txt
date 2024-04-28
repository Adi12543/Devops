pipeline {
    agent any
    
    environment {
        XAMPP_PATH = 'C:\xampp\htdocs' // Provide the path to your XAMPP htdocs directory
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
                bat "xcopy /s /y dwsample1-html.html \"${env.XAMPP_PATH}\""
                bat "xcopy /s /y dwsample2-html.html \"${env.XAMPP_PATH}\""
                bat "xcopy /s /y dwsample3-html.html \"${env.XAMPP_PATH}\""
            }
        }
    }
}


