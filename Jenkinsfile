pipeline {
  agent any
  stages {
    stage('say Hello') {
      parallel {
        stage('say Hello') {
          steps {
            sh 'echo \'Hello World\''
          }
        }

        stage('build app') {
          agent {
            docker {
              image 'gradle:6-jdk11'
              args '''- -c
- cd ci; ./build-app.sh'''
            }

          }
          steps {
            sh 'echo "gradle build app"'
          }
        }

      }
    }

  }
}