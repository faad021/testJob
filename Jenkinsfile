pipeline {
    agent {
        dockerfile true
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                docker build -t myapp .
            }
        }
    }
}
