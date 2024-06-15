pipeline {
agent any 
stages {
    stage('WORKDIR') {
        steps {
           sh 'pwd'
      }
    }
    stage('BUILD') {
        steps {
           sh 'docker build -t dine .'
      }
    }
    stage('DEPLOY') {
        steps {
           sh 'docker container run -dt --name dine-con -p 9000:80 dine'
      }
    }
  }
}
