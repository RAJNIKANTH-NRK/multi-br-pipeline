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
           sh 'docker build -t login .'
      }
    }
    stage('DEPLOY') {
        steps {
           sh 'docker container run -dt --name login -p 7000:80 login'
      }
    }
  }
}
