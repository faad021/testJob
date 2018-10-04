pipeline {
    agent { Dockerfile true }
    stages {
        stage('Clone repository') {
           checkout scm
        }
        stage('Build') {
            steps {
                docker build --name myapp .
        }
   }      
}
