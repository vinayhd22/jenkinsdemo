pipeline {
  agent any
  stages {
    stage('install jenkins') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Enable service') {
      steps {
        sh 'Sudo service apache2 start'
      }
    }

    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/vinayhd22/jenkinsdemo.git', branch: 'main', poll: true)
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}