pipeline {
    agent any

    options {
        gitLabConnection('GitLab')
    }

    triggers {
        gitlab(
            triggerOnPush: true,
            triggerOnMergeRequest: true,
            branchFilterType: 'All',
            addVoteOnMergeRequest: true)
    }
    
    stages {
        // stage('pull') {
        //     steps {
        //         git changelog: false, credentialsId: '840815d8-528b-4a41-bf8c-dd56b9e44c29', poll: false, url: 'ssh://git@gitlab.zeaho.com:10133/wengjiankai/vuetify-template.git'
        //     }    
        // }
        
        stage('Build for master') {
            when {
              branch 'master'
            }
            steps {
                echo "${OWNER} in master"
            }
        }
        
        stage('Build for dev') {
            when {
              branch 'dev'
            }
            steps {
                echo "${OWNER} in dev"
            }
        }
        
        stage('Build for release') {
            when {
              branch 'release'
            }
            steps {
                echo "${OWNER} in release"
            }
        }
    }
}