pipeline {
    agent { Dockerfile true }
    stages {
        stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

           checkout scm
        }
        stage('Build') {
            steps{
            docker build 'MvcMovie.csproj'
        }
    }
   }      
}
