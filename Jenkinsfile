pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date
'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testing steps'
          }
        }

        stage('testing 1') {
          steps {
            echo 'testing1'
          }
        }

      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploying'
          }
        }

        stage('sleep') {
          steps {
            sleep 5
          }
        }

      }
    }

  }
}