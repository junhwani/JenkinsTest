pipeline {
  stages {
    stage('Source') {
      steps {
        git(url: 'https://github.com/junhwani/JenkinsTest.git', branch: 'master')
      }
    }

    stage('Deploy') {
      steps {
        sh 'kubectl --kubeconfig .kube/config apply -f prom.yaml'
      }
    }

  }
}
