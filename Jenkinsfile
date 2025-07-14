pipeline{
    agent any
   
    stages {
        stage('compile') {
            steps {
                sh 'javac Test.java'
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