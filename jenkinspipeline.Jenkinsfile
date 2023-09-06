pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '--- Building the code ---'
                sh 'mvn clean package' // You can replace this with your build commands
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo '--- Running unit and integration tests ---'
                sh 'mvn test' // Replace with your test commands
            }
        }

        stage('Code Analysis') {
            steps {
                echo '--- Performing code analysis ---'
                // Integrate with your code analysis tool, e.g., SonarQube
                // Example: sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo '--- Performing security scan ---'
                // Integrate with your security scanning tool, e.g., OWASP ZAP
                // Example: sh 'zap-cli --quick-scan -t http://your-app-url'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo '--- Deploying to staging environment ---'
                // Use your deployment tool or script to deploy to staging, e.g., AWS CodeDeploy
                // Example: sh 'aws deploy create-deployment ...'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo '--- Running integration tests on staging environment ---'
                // Run integration tests on the staging environment
                // Example: sh 'mvn verify -Pstaging'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo '--- Deploying to production environment ---'
                // Use your deployment tool or script to deploy to production, e.g., AWS CodeDeploy
                // Example: sh 'aws deploy create-deployment ...'
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
