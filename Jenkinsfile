pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        node ('master') {
          checkout scm
        }
      }
    }

    stage('build') {
      steps {
        node ('master') {
          sh 'echo "hello ini pipeline"'
        }
      }
    }

  }
  environment {
    APP_ENV = 'production'
  }
}
