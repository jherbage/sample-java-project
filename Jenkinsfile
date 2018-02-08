pipeline {
  agent any

  stages {
    stage('Say Hello') {
       steps {
         sh 'ant -f test.xml -v'
       }
    }
  }
  
  post {
    always {
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
    }
  }
}
