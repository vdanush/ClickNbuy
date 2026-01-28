pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                    chmod +x mvnw
                    ./mvnw clean package
                '''
            }
        }

        stage('Run App') {
            steps {
                sh '''
                    nohup java -jar target/ClickNBuy-1.0.jar > app.log 2>&1 &
                '''
            }
        }
    }
}
