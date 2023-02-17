pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello'
                build 'PES1UG20CS344-1'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployement Successfull"
            }
        }
    }
    
    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
