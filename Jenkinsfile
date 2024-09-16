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
        // run Kaniko to build and push the docker image
        sh '''
                    docker run --rm -v $(pwd):/workspace \
                    -v /path/to/.docker/config.json:/kaniko/.docker/config.json:ro \
                    gcr.io/kaniko-project/executor:latest \
                    --dockerfile /workspace/Dockerfile \
                    --context /workspace \
    }
  }
}

