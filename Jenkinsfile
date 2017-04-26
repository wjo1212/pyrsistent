pipeline {
  agent any
  stages {
    stage('Package') {
      steps {
        echo 'Hello world'
        sh 'run script'
      }
    }
    stage('UT/Covearge') {
      steps {
        echo 'hello UT'
      }
    }
    stage('QA Test - Chrome') {
      steps {
        parallel(
          "QA Test": {
            echo 'hello chrome'
            
          },
          "QA Test - Firefox": {
            sh 'sh ./test.sh'
            
          }
        )
      }
    }
  }
}