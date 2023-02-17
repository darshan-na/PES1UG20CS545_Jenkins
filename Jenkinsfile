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
        sh './PES1UG20CS545'
      }
    }
    
    stage('Deploy') {
      steps {
        eho 'Deployment'
      }
    }
  }
  post {
    failure {
      eho 'Pipeline failed'
    }
  }
}
