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
           sh 'docker build -t food .'
      }
    }
    stage('DEPLOY') {
        steps {
           sh 'docker container run -dt --name food -p 9000:80 food'
      }
    }
  }
}
