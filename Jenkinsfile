pipeline {
    agent any

    stages {
        stage('Cloning Repo') {
            steps {
                git credentialsId: '1a6b09a8-52de-4845-a107-8b9c0c0f990d', url: 'https://github.com/Gates12/maven-web-app.git'
            }
        }
    }
}
