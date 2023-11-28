pipeline {
    agent any

    stages {
        stage('SCM checkout') {
            steps {
                git branch: 'main', credentialsId: 'jk-gh-tk', url: 'https://github.com/dorson38/jk-private-gh.git'
            }
        }
        
        stage('Build Docker Iamge') {
            steps {
                sh 'docker build -t dorson38/webapp:$BUID_NUMBER .'
            }
        }
    }
}
