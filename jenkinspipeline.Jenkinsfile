pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo '--- Building the code ---'
                echo 'Building MVN...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo '--- Running unit and integration tests ---'
                echo 'Running  Maven tests...'
            }
        }
        stage('Code Analysis') {
            steps {
                echo '--- Performing code analysis ---'
                echo 'Performing code analysis...'
            }
        }
        stage('Security Scan') {
            steps {
                echo '--- Performing security scan ---'
                echo 'Performing security scan...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo '--- Deploying to staging environment ---'
                echo 'Deploying to staging environment...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo '--- Running integration tests on staging environment ---'
                echo 'Running integration tests on staging environment...'
            }
      post {
                success {
                    echo '--- Unit and Integration Tests Successful ---'
                    // Send success notification email for tests
                    emailext subject: 'Unit and Integration Tests Successful',
                        body: 'The unit and integration tests have completed successfully.',
                        to: 'your-email@example.com'
                }
                failure {
                    echo '--- Unit and Integration Tests Failed ---'
                    // Send failure notification email for tests
                    emailext subject: 'Unit and Integration Tests Failed',
                        body: 'The unit and integration tests have failed. Please check the logs for details.',
                        to: 'your-email@example.com'
                }
            }
}
        stage('Deploy to Production') {
            steps {
                echo '--- Deploying to production environment ---'
                echo 'Deploying to production environment...'
            }
        }
    }
   
   
