pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "building ${env.GIT_BRANCH}"'
        sh 'npm install'
      }
    }

  }
}