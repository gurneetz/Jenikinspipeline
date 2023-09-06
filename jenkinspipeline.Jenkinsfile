pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo '--- Building the code ---'
                // Add build commands here (e.g., Maven)
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo '--- Running unit and integration tests ---'
                // Add testing commands here (e.g., Maven test)
            }
        }
        stage('Code Analysis') {
            steps {
                echo '--- Performing code analysis ---'
                // Add code analysis tool commands here
            }
        }
        stage('Security Scan') {
            steps {
                echo '--- Performing security scan ---'
                // Add security scanning tool commands here
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo '--- Deploying to staging environment ---'
                // Add deployment commands here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo '--- Running integration tests on staging environment ---'
                // Add integration tests on staging commands here
            }
        }
        stage('Deploy to Production') {
            steps {
                echo '--- Deploying to production environment ---'
                // Add deployment to production commands here
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
            mail to: 'Gurneets.in@gmail.com',
                subject: 'Pipeline Failed',
                body: 'The Jenkins pipeline has failed. Please check the logs for details.'
        }
    }
}
