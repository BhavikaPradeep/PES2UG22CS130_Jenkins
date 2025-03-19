pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main/hello.cp -o main/hello_exec'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './main/hello_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
