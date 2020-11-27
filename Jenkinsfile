pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build demo-app'
      }
    }

    stage('Linux Tests') {
      parallel {
        stage('Linux Tests') {
          steps {
            echo 'Run Linux Tests'
          }
        }

        stage('Windows Tests') {
          steps {
            echo 'Run Windows Tests'
          }
        }

      }
    }

    stage('Deploy Staging') {
      steps {
        echo 'Deploy to staging environment'
        input 'Ok to deploy to production?'
      }
    }

  }
}