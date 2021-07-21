pipeline {

 agent any //{ label 'kubepod' }

  stages {
    stage('Checkout Source') {
      steps {
        git url:'https://github.com/krish0337/helm.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
       // script {
         // kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        //}
    sh """ 
     
    /usr/local/bin/kubectl  get pods 
    /usr/local/bin/kubectl create -f nginx.yaml 
     /usr/local/bin/kubectl get pods 
     /usr/local/bin/helm list
     kubectl get pods
     helm list
    
    
    """
      }
    }

  }
}
