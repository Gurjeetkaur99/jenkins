pipeline {
    agent any
    stages {
        stage('Checkout from Git') {
            steps {
                git branch: 'prod', url: 'https://github.com/Gurjeetkaur99/jenkins.git'
            }
        }
    }
}