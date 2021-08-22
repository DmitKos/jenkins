pipeline {
    agent any
    triggers {
        pollSCM('H/5 * * * *')
    }
    stages {
        stage('First') {
            steps {
                sh 'tail /var/log/jenkins/jenkins.log'
            }
        }
    }
}