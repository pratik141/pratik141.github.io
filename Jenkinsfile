pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('shell') {
      steps {
        sh 'echo hi '
      }
    }
    stage('ee') {
      steps {
        parallel(
          "ee": {
            echo 'ccc'
            
          },
          "ff": {
            sh 'echo ok '
            
          }
        )
      }
    }
  }
}