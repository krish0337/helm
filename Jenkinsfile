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
     
    /usr/local/bin/kubectl  get pods 
    /usr/local/bin/kubectl install nginx
     sleep 3
     /usr/local/bin/kubectl get pods 
     /usr/local/bin/helm list
     kubectl get pods
     helm list
    
    
    """
      }
    }

  }
}
