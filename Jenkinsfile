pipeline {
    agent {
        label 'master'
    }
    
    stages {
        stage('Initialize') {
            steps{
                slackSend channel: 'jenkins-workshop', message: 'Initializing job'
            }
        }
        
        stage('Deploy project') {
            steps {
                slackSend channel: 'jenkins-workshop', message: 'Building ...'
                sh "fastlane android deploy_dev --env development"
            }
        }
    }
}
