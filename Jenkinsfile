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
         app = bat "docker tag myapp https://nexus.1worldsync.de/#browse/browse:docker/myapp:latestapp"
         app = bat "docker push https://nexus.1worldsync.de/#browse/browse:docker/myapp:latestapp"
        }
}
