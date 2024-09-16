pipeline{
  agent only
  
  stages{
    stage('Checkout'){
      steps{
        // checkout the code from GitHub
        git url: 'https://github.com/r1031/kaniko.git', branch: 'dev'
      }
    }
    stage("build"){
      script {
        // build and push the docker image
        def image = docker.build("kaniko:latest")
    }
  }
}

