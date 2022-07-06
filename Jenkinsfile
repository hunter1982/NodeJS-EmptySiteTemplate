pipeline {
  agent {
    node {
      label 'centrosSlave'
    }

  }
  stages {
    stage('Checkout code') {
      parallel {
        stage('Checkout code') {
          steps {
            git(url: 'https://github.com/hunter1982/NodeJS-EmptySiteTemplate.git', branch: 'master', credentialsId: 'github')
          }
        }

        stage('Say Hello') {
          steps {
            sh 'echo "Hello"'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

  }
}