pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/parvez76/nodejs_with_jenkins', branch: 'main')
      }
    }

    stage('shell') {
      parallel {
        stage('shell') {
          steps {
            sh 'ls -la'
          }
        }

        stage('unit test') {
          steps {
            sh 'cd nodeapp/node-1 && npm i runt test:unit'
          }
        }

      }
    }

  }
}