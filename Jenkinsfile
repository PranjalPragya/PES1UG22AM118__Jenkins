pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/PranjalPragya/PES1UG22AM118__Jenkins.git'
            }
        }

        stage('Build') {
            steps {
                sh 'g++ new.cpp -o output'
                echo 'Build stage successful'
            }
        }

        stage('Test') {
            steps {
                sh './main/output'
                echo 'Test stage successful'
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
            echo 'Pipeline failed'
        }
    }
}
