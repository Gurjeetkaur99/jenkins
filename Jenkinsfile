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
        stage('Terraform Init') {
            steps {
                script {
                    sh 'terraform init'
                }
            }
        }
        stage('Terraform validate') {
            steps {
                script {
                    sh 'terraform validate'
                }
            }
        }
        stage('Terraform plan') {
            steps {
                script {
                    sh 'terraform plan'
                }
            }
        }
        stage('Terraform apply') {
            steps {
                script {
                    sh 'terraform apply --auto-approve'
                }
            }
        }
        stage('Approve to destroy') {
            steps {
                input message: 'Approve to Destroy', ok: 'Destroy'
            }
        }
        stage('Terraform destroy') {
            steps {
                script {
                    sh 'terraform destroy --auto-approve'
                }
            }
        }
    }
}