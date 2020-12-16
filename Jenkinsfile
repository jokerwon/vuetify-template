pipeline {
    agent any
    
    stages {
        stage('pull') {
            steps {
                git changelog: false, credentialsId: '840815d8-528b-4a41-bf8c-dd56b9e44c29', poll: false, url: 'ssh://git@gitlab.zeaho.com:10133/wengjiankai/vuetify-template.git'
            }    
        }
        
        stage('build') {
            steps {
                echo "${OWNER}"
            }
        }
    }
}