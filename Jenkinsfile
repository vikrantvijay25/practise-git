pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/vikrantvijay25/practise-git.git', branch: 'main', credentialsId: 'ocen_git', poll: true, changelog: true)
      }
    }

    stage('Install Apache') {
      steps {
        sh 'echo "test"'
      }
    }

    stage('deploy code') {
      steps {
        sh 'echo "Deploying code."'
      }
    }

  }
}