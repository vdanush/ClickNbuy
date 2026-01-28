pipeline{
    agent any
      tools {
        maven 'maven'
      }
     stages {
        stage('Hello') {
            steps {
               sh 'mvn clean package'
           }
          stage('Run App') {
    steps {
        sh 'nohup java -jar target/*.jar &'
    }
   }
  }
 }
}
