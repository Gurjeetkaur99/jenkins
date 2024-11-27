pipeline {
    agent any
    stages {
        stage('Checkout from Git') {
            steps {
                git branch: 'main', credentialsId: 'git-cred', url: 'https://github.com/Gurjeetkaur99/jenkins.git'
            }
        }
        stage('Terraform version') {
            steps {
                script {
                    sh 'terraform verison'
                }
            }
        }
   }
}