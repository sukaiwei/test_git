pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/jenkins_demo') {
          git 'git@github.com:sukaiwei/test_git.git'
        }

      }
    }
    stage('build') {
      steps {
        sh 'sudo -H pip install -r requirements.txt'
      }
    }
    stage('run') {
      steps {
        sh 'python app.py'
      }
    }
  }
}