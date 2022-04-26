pipeline {
  agent {
    docker {
      image "python:3.7"
    }
  }
  
  stages {
    stage ('Enviornment preparation') {
      steps {
        echo "-=- preparing project enviornment -=-"
        // Python dependencies
        sh "pip install -r requirements.txt"
      }
    }
    stage ('Build Docker image') {
      steps {
        echo "-=- build Docker image -=-"
        sh "docker build -t e19cse009/python-jenkins-pipeline:0.1 ."
      }
    }
    stage ("Run Docker image") {
      steps {
        echo "-=- run Docker image -=-"
        sh "docker run e19cse009/python-jenkins-pipeline:0.1 ."
      }
    }
  }
}
    
