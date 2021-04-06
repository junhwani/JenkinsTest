pipeline {
  agent {
    node {
      label 'Agent'
    }

  }
  stages {
    stage('Source') {
      steps {
        git(url: 'https://github.com/junhwani/JenkinsTest.git', branch: 'master')
      }
    }

  }
}