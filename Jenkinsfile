node {
  def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = bat "docker build -t myapp.zip ."
    }
    stage('Test image') {
         bat 'echo "Tests successful"'
        }
    stage('Zip image') {
         app =bat 'echo test > archive/test.txt'
         app =zip archive: true, dir: 'archive', glob: '', zipFile: 'myapp.zip'
        }
     stage('Push image') {
       withDockerRegistry([ credentialsId: "", url: "https://hub.docker.com/r/fsayaou/jenkinstest/" ]) {
         
         app = bat "docker login"
         app = bat "docker tag myapp.zip fsayaou/jenkinstest:myapp.zip"
         app = bat "docker push fsayaou/jenkinstest:myapp.zip"
        }
  }
}
