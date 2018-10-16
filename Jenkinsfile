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
          git(url: 'git@github.com:sukaiwei/test_git.git', credentialsId: 'ae44a2d1-dd0f-4a77-a816-507c5f81eaee')
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