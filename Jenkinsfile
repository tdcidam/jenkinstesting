pipeline {
  agent any
  parameters {
        booleanParam(defaultValue: true, description: '', name: 'host1')
    }
  stages {
    stage('Pull Git Repository') {
      steps {
        git(url: 'ssh://git@stash.kp.org/infra/iam-11g.git', branch: 'master', credentialsId: 'Stash')
      }
    }
    stage('Print Message') {
      when{
        expression { params.host1 == 'host2' }
      }
      steps {
        echo 'HI '
        sh 'echo "Hi from Declarative pipeline script"'
      }
    }
  }
}
