pipeline {
  agent any
  stages {
    stage('step1') {
      steps {
        echo 'hoge'
      }
    }
    stage('step2') {
      steps {
        sh '''echo " hoge"
pwd
ls

echo $PATH

which ls
ls /usr/local/bin
'''
      }
    }
    stage('dockerstep') {
      agent {
        docker {
          image 'alpine'
        }
        
      }
      steps {
        sh 'ls'
      }
    }
  }
}