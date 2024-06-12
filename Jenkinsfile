pipeline {
agent any 
stages {
    stage('containers') {
        steps {
           sh 'docker container ls'
      }
    }
    stage('build') {
        steps {
           sh 'docker build -t ecomm .'
      }
    }
    stage('deploy') {
        steps {
           sh 'docker container run -dt --name ecomm-con -p 60:80 ecomm'
      }
    }
  }
}
