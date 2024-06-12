pipeline {
agent any 
stages {
    stage('WORKDIR') {
        steps {
           sh 'pwd'
      }
    }
    stage('build') {
        steps {
           sh 'docker build -t food .'
      }
    }
    stage('deploy') {
        steps {
           sh 'docker container run -dt --name food-con -p 90:80 food'
      }
    }
  }
}
