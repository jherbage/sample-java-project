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
      archive 'dist/*.jar'
    }
  }
}
