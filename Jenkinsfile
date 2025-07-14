pipeline{
    agent any
    environment {
        JAVA_VERSION = '21.0'
    }
    stages {
        stage('compile') {
            steps {
                sh 'javac Test.java'
                sh 'echo &{JAVA_VERSION}'
            }
        }
        stage('run') {
            steps {
                sh 'java Test'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}