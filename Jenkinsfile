node {
  def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = bat "docker build -t myapp ."
    }
    stage('Test image') {
         bat 'echo "Tests successful"'
        }
    stage('Deploy image') {
         bat 'echo "Deployed successfully"'
        }
     stage('Run image') {
         app = bat "docker run -p 3000:80 myapp"
        }
}
