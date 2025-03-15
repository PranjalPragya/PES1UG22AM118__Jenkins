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
                sh 'g++ main/hello.cpp -o main/output'
                echo 'Build stage successful'
            }
        }

        stage('Test') {
            steps {
                sh './non_existent_file'  // Intentional error
                echo 'Test Stage Completed'
            }
        }


        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
                // Add actual deployment steps if required
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
