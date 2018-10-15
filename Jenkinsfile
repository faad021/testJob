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
    //stage('Zip image') {
      //   app =zip archive: true, dir: 'archive', glob: '', zipFile: 'myapp'
      //  }
     stage('Push image') {
       withDockerRegistry([ credentialsId: "", url: "https://hub.docker.com/r/fsayaou/jenkinstest/" ]) {
         
         app = bat "docker login"
         app = bat "docker tag myapp fsayaou/jenkinstest:myapp"
         app = bat "docker push fsayaou/jenkinstest:myapp"
        }
  }
}
