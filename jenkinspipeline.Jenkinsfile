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
        }
        stage('Deploy to Production') {
            steps {
                echo '--- Deploying to production environment ---'
                echo 'Deploying to production environment...'
            }
        }
    }
   
   post {
        success {
            echo '--- Pipeline Successful ---'
            // Send success notification email with logs as attachment
                mail to: 'Gurneets.in@gmail.com',
                subject: 'Pipeline Successful',
                body: 'The Jenkins pipeline has completed successfully.'
                
        }
        failure {
            echo '--- Pipeline Failed ---'
            // Send failure notification email with logs as attachment
                mail to: 'Gurneets.in@gmail.com'

                subject: 'Pipeline Failed',
                body: 'The Jenkins pipeline has failed. Please check the logs for details.',
             
        }
    }

