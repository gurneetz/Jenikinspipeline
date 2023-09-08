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
                    script {
                        // Capture the build log
                        def buildLog = readFile('build.log')

                        emailext subject: 'Tests Completed',
                            body: 'Unit and integration tests have completed.',
                            to: 'Gurneets.in@gmail.com',
                            attachLog: true // Attach the current step's log
                            attachmentsPattern: '**/build.log' // Attach the build log
                    }
                }
            }
        }
        // ... Other stages ...
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
