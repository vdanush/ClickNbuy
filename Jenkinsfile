pipeline {
    agent any
    tools {
        jdk 'Java'
        maven 'Maven'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }
        stage('Run App') {
            steps {
                sh 'nohup java -jar target/ClickNBuy-1.0.jar > app.log 2>&1 &'
            }
        }
    }
}
