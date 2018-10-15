pipeline {
  agent none
  stages {
    stage('git') {
      steps {
        dir(path: '/home/sukaiwei/test_git') {
          git 'git@github.com:sukaiwei/test_git.git'
        }

      }
    }
  }
}