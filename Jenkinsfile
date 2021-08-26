// for example
pipeline {
    agent any
    triggers {
        pollSCM('H/15 * * * *')
    }
    stages {
        stage('First') {
            steps {
                sh 'tail /var/log/jenkins/jenkins.log'
            }
        }
        stage('Second') {
            steps {
                sh 'ls -lS /home'
            }
        }
        stage('Third') {
            steps {
                sh 'ls -lS /home/json_exporter'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*', fingerprint: true
        }
    }
}
