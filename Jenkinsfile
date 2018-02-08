pipeline {
  agent any
  
  environment {
    MAJOR_VERSION = 1
  }

  stages {
    stage('Say Hello') {
       steps {
         sh 'ant -f build.xml -v'
       }
    }
  }
  
  post {
    always {
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
    }
  }
}
