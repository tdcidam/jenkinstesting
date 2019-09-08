pipeline {
  agent any
  stages {
    stage('Pull Git Repository') {
      steps {
        git(url: 'ssh://git@stash.kp.org/infra/iam-11g.git', branch: 'master', credentialsId: 'Stash')
      }
    }
  }
}