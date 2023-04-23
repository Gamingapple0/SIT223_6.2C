pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
    post {
        always {
            mail to:"madhikarmianshu@gmail.com",
            subject: "Integration Test",
            body: "Build Sucessful"
        }
    }
}
