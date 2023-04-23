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
            subject: "${currentBuild.result}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'", 
            to: 'madhikarmianshu@gmail.com',
            body: 'Build Sucessful'
        }
    }
}
