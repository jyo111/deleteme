pipeline {
    agent any    
    stages {
        stage('SCM checkout') {
            steps {
                git 'https://github.com/jyo111/deleteme.git'
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
