pipeline {

  agent any
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/srinivas1981/hipster-shop.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          sh 'sudo /usr/local/bin/kubectl apply -f release/kubernetes-manifests.yaml -n cartshopping12'
        }
      }
    }

  }

}
