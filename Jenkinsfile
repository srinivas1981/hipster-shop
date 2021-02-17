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
      //sh 'sudo /usr/local/bin/kubectl create ns cart --kubeconfig=/var/aws-config-workload/admin.conf'
      sh 'sudo /usr/local/bin/kubectl apply -f release/kubernetes-manifests.yaml -n cart --kubeconfig=/var/aws-config-workload/admin.conf'                    
}
      }
    }

  }

}
