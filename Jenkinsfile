pipeline{
    agent any
    stages{
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests using JUnit and Selenium'
            }
            post{
                always{
                    mail to: "madhikarmianshu@gmail.com",
                    subject: "Unit Test Status Email",
                    body: "Build log attached!"
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing the code using Jenkins and SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing a security scan on the code using OWASP ZAP'
            }
            post{
                always{
                    mail to: "madhikarmianshu@gmail.com",
                    subject: "Security Scan Email",
                    body: "${currentBuild.result}: Job "
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium'
            }
            post{
                always{
                    mail to: "madhikarmianshu@gmail.com",
                    subject: "Integration Test Status Email",
                    body: "'${env.JOB_NAME} [${env.BUILD_NUMBER}]'"
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to an AWS EC2 instance'
            }
        }
    }

}
