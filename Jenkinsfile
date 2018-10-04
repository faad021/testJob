node {
  def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = bat "docker build -t myapp ."
    }
    stage('Test image') {
         app.inside {
            bat 'echo "Tests passed"'
        }
       
        }
}
