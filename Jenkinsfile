pipeline {

 agent any //{ label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Netra-sh/helm.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
       // script {
         // kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        //}
    sh """ 
      chmod u+x ./kubectl
     ./kubectl delete -f nginx.yml
     sleep 3
     ./kubectl get pods 
     ./kubectl create -f nginx.yml 
     sleep 3
     ./kubectl get pods 
    
    """
      }
    }

  }
}
