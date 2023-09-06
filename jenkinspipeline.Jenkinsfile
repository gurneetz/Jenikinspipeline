pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Add build commands here (e.g., Maven)
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Add testing commands here (e.g., Maven test)
            }
        }
        stage('Code Analysis') {
            steps {
                // Add code analysis tool commands here
            }
        }
        stage('Security Scan') {
            steps {
                // Add security scanning tool commands here
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Add deployment commands here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Add integration tests on staging commands here
            }
        }
        stage('Deploy to Production') {
            steps {
                // Add deployment to production commands here
            }
        }
    }
    post {
        success {
            // Send success notification email with logs as attachment
            emailext subject: 'Pipeline Successful',
                body: 'The Jenkins pipeline has completed successfully.',
                to: 'Gurneets.in@gmail.com'
        }
        failure {
            // Send failure notification email with logs as attachment
            emailext subject: 'Pipeline Failed',
                body: 'The Jenkins pipeline has failed. Please check the logs for details.',
                to: 'Gurneets.in@gmail.com'
        }
    }
}
