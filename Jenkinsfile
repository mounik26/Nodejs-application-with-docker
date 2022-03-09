pipeline {
  agent any
    
  tools {nodejs "NodeJS"}
    
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

