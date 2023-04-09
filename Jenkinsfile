pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        script {
          // Build the Docker image
           docker build -t hello-world-app .
           docker push <your-repo-username>/hello-world-app
        }
      }
    }
    
    stage('Deploy') {
      steps {
        script {
          // Deploy the Docker image to the Kubernetes cluster
          sh "kubectl apply -f app-deployment.yaml"
        }
      }
    }
  }
}