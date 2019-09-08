pipeline {
  agent any
  stages {
    stage('Pull Git Repository') {
      steps {
        git(url: 'ssh://git@stash.kp.org/infra/iam-11g.git', branch: 'master', credentialsId: 'Stash')
      }
    }
    stage('Print Message') {
      when{
        expression { params.host1 == 'host1' }
      }
      steps {
        echo 'HI '
        sh 'echo "Hi from Declarative pipeline script"'
      }
    }
  }
}
