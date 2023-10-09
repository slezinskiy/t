pipeline {
    agent any
    environment {
        GIT_MESSAGE = """${sh(
            script: 'git log --no-walk --format=format:%s ${GIT_COMMIT}', 
            returnStdout: true
            )}"""
    }
    stages {
        stage('test') {
            steps {
                sh 'echo "Message: --${GIT_MESSAGE}--"'
            }
        }
    }
}
