pipeline {
agent any 
stages {
    stage('CONTAINER') {
        steps {
           sh 'docker container ls'
      }
    }
    stage('BUILD') {
        steps {
           sh 'docker build -t ecomm .'
      }
    }
    stage('DEPLOY') {
        steps {
           sh 'docker container run -dt --name ecomm -p 8000:80 ecomm'
      }
    }
  }
}
