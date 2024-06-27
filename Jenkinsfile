pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/PratikshaKun10/CI-CD-pipeline-for-Simple-Web-Application.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker build -t your-app .'
                sh 'docker run -d -p 8080:8080 your-app'
            }
        }
    }
}
