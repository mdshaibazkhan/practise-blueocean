pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/mdshaibazkhan/practise-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo install apache2 -y'
      }
    }

    stage('deploy code') {
      steps {
        sh 'sudo -R * /var/www/html'
      }
    }

  }
}