pipeline {
  agent any
  stages {
    stage('staging') {
      steps {
        echo 'code is in staging'
        sh '''pwd 
date 
ls
'''
      }
    }

    stage('testing') {
      parallel {
        stage('testing') {
          steps {
            echo 'code is in testing'
          }
        }

        stage('error') {
          steps {
            echo 'done'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}