pipeline {
    agent any
    
    tools{
        maven 'Maven-3.9.11'
    }
    stages {
        stage('clone') {
            steps {
                git credentialsId: '1a6b09a8-52de-4845-a107-8b9c0c0f990d', url: 'https://github.com/Gates12/maven-web-app.git'
            }
        }
        stage('build'){
            steps{
                 sh 'mvn clean package'
            }
        }
        stage('docker image'){
            steps {
                sh 'docker build -t gates/mavenwebapp .'
            }
        }
        stage('k8s deploy'){
            steps{
               sh 'kubectl apply -f k8s-deploy.yml'
            }
        }
    }
}
