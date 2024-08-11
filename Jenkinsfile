pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/vikrantvijay25/practise-git.git', branch: 'main', credentialsId: 'ocen_git', poll: true, changelog: true)
      }
    }
stage('Run Snyk') {
      steps {
        sh 'echo "running snyk"'
        snykSecurity snykInstallation: 'Please define a Snyk installation in the Jenkins Global Tool Configuration. This task will not run without a Snyk installation.', snykTokenId: 'snyk token id'
      }
    }
    stage('Install Apache') {
      steps {
        sh 'echo "test"'
        sh 'sudo apt install apache2'
      }
    }

    stage('deploy code') {
      steps {
        sh 'echo "Deploying code."'
        sh 'sudo cp -R * /var/www/html'
      }
    }

  }
}
