pipeline {
    agent any
    tools {
        maven 'maven-3'
    }
    stages {
        stage('compile-package') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('slack notification') {
            steps {
                slackSend baseUrl: 'https://hooks.slack.com/services/',
                channel: 'jyothichannel',
                color: 'good',
                message: 'slack notification successful',
                tokenCredentialId: 'slack-demo',
                username: 'jyothi'
            }
        }

    }
}
