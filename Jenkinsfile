pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the application code.'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests.'
                echo 'Tools: JUnit and Selenium'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse the code and check that it meets industry standards.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan the application code for security vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to the staging environment.'
                echo 'Tool: AWS CLI with an AWS EC2 staging server'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests in the staging environment.'
                echo 'Tool: Postman Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the approved application to the production environment.'
                echo 'Tool: AWS CLI with an AWS EC2 production server'
            }
        }
    }
}
