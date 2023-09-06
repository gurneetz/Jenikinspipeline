pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Starting Build stage...'
                // Add build commands here (e.g., Maven)
                echo 'Build completed.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
                // Add testing commands here (e.g., Maven test)
                echo 'Tests completed.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis...'
                // Add code analysis tool commands here
                echo 'Code analysis completed.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
                // Add security scanning tool commands here
                echo 'Security scan completed.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                // Add deployment commands here
                echo 'Deployment to staging completed.'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment...'
                // Add integration tests on staging commands here
                echo 'Integration tests on staging completed.'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
                // Add deployment to production commands here
                echo 'Deployment to production completed.'
            }
        }
    }
    post {
        success {
            // Send success notification email with logs as attachment
            emailext subject: 'Pipeline Successful',
                body: 'The Jenkins pipeline has completed successfully.',
                to: 'Gurneetgarry.in@gmail.com'
        }
        failure {
            // Send failure notification email with logs as attachment
            emailext subject: 'Pipeline Failed',
                body: 'The Jenkins pipeline has failed. Please check the logs for details.',
                to: 'Gurneetgarry.in@gmail.com'
        }
    }
}
