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
          discordSend description: "Jenkins Pipeline Build", footer: "Footer Text", link: env.BUILD_URL, result: currentBuild.currentResult, title: JOB_NAME, webhookURL: "https://discord.com/api/webhooks/1111518532572827699/GgzM64sLXaCEepeAwddU4UEt_YpHZxxMNPIpcpWUZynRbmQvfK1VsRWsLPs3ZTDJRFoL"
        }
      }
    }

  }
  environment {
    APP_ENV = 'production'
  }
}
