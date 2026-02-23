pipeline {
    agent any

    tools {
        maven 'Maven-3.9.12'
        jdk 'JDK-21'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Aditya12345-byte/devops2.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                bat 'copy target\\*.war C:\\xampp\\tomcat\\webapps'
            }
        }
    }
}