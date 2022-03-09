spipeline {
  agent any
    
  tools {nodejs "nodejs"}
    
  stages {
        
    stage('Build') {
      steps {
        sh """
        docker build -t kiyansh26/nodejs-pipeline-01 -f Dockerfile .
        docker push kiyansh26/nodejs-pipeline-01
        docker run -p 9000:9000 -d --name node-js-pipeline kiyansh26/nodejs-pipeline-01:latest
        """
      }
    }  
    
  }
}

