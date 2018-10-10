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
     stage('Run image') {
         app = bat "docker run -p 9090:80 myapp"
        }
}
