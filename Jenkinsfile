pipeline {
  agent any
  stages {
    stage('install') {
      parallel {
        stage('install') {
          agent any
          steps {
            sh 'sudo yum install -y dhcp'
          }
        }

        stage('mkdir') {
          agent any
          steps {
            sh 'sudo mkdir /test'
          }
        }

      }
    }

    stage('rmdir') {
      steps {
        sh 'rm -rf /test'
      }
    }

  }
}