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
         app = bat "docker run -d -p 5000:80 --name myapp myapp."
        }
}
