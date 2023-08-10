pipeline {
  agent any
  tools{
    gradle 'gradle'
  }
  stages {
    stage('say Hello') {
      parallel {
        stage('say Hello') {
          steps {
            sh 'echo \'Hello World\''
          }
        }

        stage('build app') {
          agent any
          steps {
            sh 'cd ci && ./build-app.sh'
          }
        }

      }
    }

  }
}
