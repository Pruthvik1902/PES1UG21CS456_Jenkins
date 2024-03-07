pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS456-1'
                sh 'g++ main/new123.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Display'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
