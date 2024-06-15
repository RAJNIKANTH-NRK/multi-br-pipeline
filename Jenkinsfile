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
           sh 'docker build -t cloths .'
      }
    }
    stage('DEPLOY') {
        steps {
           sh 'docker container run -dt --name cloths-con -p 8000:80 cloths'
      }
    }
  }
}
