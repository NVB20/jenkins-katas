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
              image 'gradle:latest'
            }

          }
          steps {
            sh 'cd ci && ./build-app.sh'
          }
        }

      }
    }

  }
}