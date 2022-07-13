pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        echo 'Hello World'
      }
    }
  }
  stages {
    stage('Test') {
      steps {
        echo 'Testing Hello World'
      } 
    } 
  } 
  stages {
    stage('Deploy') {
      steps {
        echo 'Deploying Hello World'
      } 
    } 
  } 
  post {
    always {
        junit(
          allowEmptyResults: true, 
          testResults: '**/build/test-results/test/*.xml'
        )
    }
  }
}
