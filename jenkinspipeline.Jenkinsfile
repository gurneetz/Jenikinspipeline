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
            post {
                success {
                    emailext subject: 'Security Scan Successful',
                        body: 'Security scan has completed successfully.',
                        to: 'Gurneets.in@gmail.com',
                        mimeType: 'text/plain',
                        attachLog: true // Attach build log
                }
                failure {
                    emailext subject: 'Security Scan Failed',
                        body: 'Security scan has failed.',
                        to: 'Gurneets.in@gmail.com',
                        mimeType: 'text/plain',
                        attachLog: true // Attach build log
                        attachmentsPattern: '**/build.log'
                }
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
                    emailext subject: 'Unit and Integration Tests Successful',
                        body: 'Unit and integration tests have completed successfully.',
                        to: 'Gurneets.in@gmail.com',
                        mimeType: 'text/plain',
                        attachLog: true // Attach build log
                }
                failure {
                    emailext subject: 'Unit and Integration Tests Failed',
                        body: 'Unit and integration tests have failed.',
                        to: 'Gurneets.in@gmail.com',
                        mimeType: 'text/plain',
                        attachLog: true // Attach build log
                        attachmentsPattern: '**/build.log'
                }
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
   
    post {
        success {
            echo '--- Pipeline Successful ---'
          
        }
        failure {
            echo '--- Pipeline Failed ---'
        
        }
    }
}
