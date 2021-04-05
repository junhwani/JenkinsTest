pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/junhwani/JenkinsTest.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
//         script {
          kubernetesDeploy(configs: "prom.yaml", kubeconfigId: "mykubeconfig")
//           kubernetesDeploy(configs: "gra.yaml", kubeconfigId: "mykubeconfig")
//         }
        sh "kubectl --kubeconfig=/root/.jenkins/.kube/config apply -f prom.yaml"
      }
    }

  }

}
