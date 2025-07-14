pipeline{
    agent any
   environment {
        JAVA_VERSION = '21.0'
        PATH = "${env.JAVA_HOME}/bin:${env.PATH}"
    }
    stages {
        stage('compile') {
            steps {
                sh 'javac Test.java'
                echo '${JAVA_VERSION}'
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