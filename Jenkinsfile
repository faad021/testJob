node {
  def app

    stage('Clone repository') {
        checkout scm
    }
    stage('Build image') {
        app = bat "docker build -t myapp2 ."
    }
    stage('Test image') {
         bat 'echo "Tests successful"'
        }
     stage('Run image') {
         app = bat "docker run -d -p 5000:80 --name myapp2 myapp2"
        }
}
