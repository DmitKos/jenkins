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
    }
}