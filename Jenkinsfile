pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "Message: --${GIT_MESSAGE}--"'
          }
        }

        stage('') {
          steps {
            echo 'rewtg'
          }
        }

      }
    }

  }
  environment {
    GIT_MESSAGE = """${sh(
                  script: 'git log --no-walk --format=format:%s ${GIT_COMMIT}', 
                  returnStdout: true
                  )}"""
    }
  }