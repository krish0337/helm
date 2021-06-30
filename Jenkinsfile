node

{

   def buildNumber = BUILD_NUMBER

   stage("Git CheckOut"){

        git url: 'https://github.com/Netra-sh/helm-charts.git',branch: 'master'

    }

   stage("Build nginx") {

         sh "helm install my-release nginx-stable/nginx-ingress "
         sh "kubectl get deployments"
   
    }

 }   
  
