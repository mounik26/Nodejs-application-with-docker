pipeline {
  agent any
    
  tools {nodejs "nodejs"}
    
  stages {
        
    stage('Build') {
      steps {
        sh """
        docker build -t kiransun1/nodejs-pipeline-01 -f Dockerfile .
        docker push kiransun1/nodejs-pipeline-01
        docker run -p 3032:9005 -d --name node-js-pipeline kiransun1/nodejs-pipeline-01:latest
        """
      }
    }  
    
  }
}

