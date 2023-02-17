pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps {
        sh 'g++ PES1UG20CS545.cpp -o PES1UG20CS545'
        build job: 'PES1UG20CS545-1'
      }
    }
    
    stage('Test') {
      steps {
        './PES1UG20CS545'
      }
    }
    
    stage('Deploy') {
      steps {
        echo 'Deployment'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
