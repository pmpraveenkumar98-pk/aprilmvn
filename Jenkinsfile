pipeline {

    agent any

    tools {
        maven 'Maven-3'
    }
    
    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/pmpraveenkumar98-pk/aprilmvn.git'
            }
        }
    
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'java -jar target/cicr-demo-1.0.jar'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }
    }
}
