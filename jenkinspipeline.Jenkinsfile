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
                echo 'Running Maven tests...'
            }
            post {
                always {
                    echo '--- Sending email notification after tests ---'
                    emailext subject: 'Tests Completed',
                        body: 'Unit and integration tests have completed.',
                        to: 'Gurneets.in@gmail.com',
                        attachLog: true // Attach the current step's log
                        attachFile: '*build.log' // Attach the build log
                }
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
            post {
                always {
                    echo '--- Sending email notification after security scan ---'
                    emailext subject: 'Security Scan Completed',
                        body: 'Security scan has completed.',
                        to: 'Gurneets.in@gmail.com',
                        attachLog: true // Attach the current step's log
                        attachFile: '*build.log' // Attach the build log
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
