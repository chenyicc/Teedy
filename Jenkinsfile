pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('K8s') {
      steps {
        sh 'kubectl set image deployments/hello-node lab12=cyic/lab12:v1.0'
      }
    }
  }
}

