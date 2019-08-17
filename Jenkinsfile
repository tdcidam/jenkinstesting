pipeline {
  agent any
  stages {
    stage('Stage1') {
      parallel {
        stage('Stage1') {
          steps {
            sh 'echo \'Hello Stage1\''
          }
        }
        stage('Step1') {
          steps {
            sh 'echo \'Step1\''
          }
        }
        stage('Step2') {
          steps {
            echo 'Hello Stage2'
          }
        }
        stage('Step3') {
          steps {
            sh 'echo \'Step3\''
          }
        }
      }
    }
    stage('Stage2') {
      parallel {
        stage('Stage2') {
          steps {
            echo 'Executing Stage2'
          }
        }
        stage('Step1') {
          steps {
            echo 'Executing Step1 in Stage2'
          }
        }
        stage('Step2') {
          steps {
            echo 'Executing Step2 in Stage2'
          }
        }
        stage('Step3') {
          steps {
            echo 'Executing Step3 in Stage2'
          }
        }
      }
    }
  }
  environment {
    Var1 = ''
    Var2 = ''
    Var3 = ''
  }
}