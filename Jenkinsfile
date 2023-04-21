pipeline {
    agent any
    stages {
        stage ('Build Dockerfile') {
            steps {

               sh 'docker build -t akin4dada/second-dockerfile:1.0 .' 
            }


        }


        stage ('Docker login') {
            steps {

               sh 'docker login --username akin4dada --password Akinola@34' 
            }


        }

        stage ('Docker Push into repository') {
            steps {

               sh 'docker push akin4dada/second-dockerfile:1.0' 
            }


        }

        stage ('minikube start') {
            steps {

               sh 'minikube start' 
            }


        }


        stage ('Create Deployment') {
            steps {

               sh 'kubectl create -f second-dockerfile.yml' 
            }


        }
    


        stage ('Create Service') {
            steps {

               sh 'kubectl create -f second-dockerfile-service.yml' 
            }


        }




        stage ('Get pods') {
            steps {

               sh 'kubectl get pods' 
            }


        }



        stage ('Show service') {
            steps {

               sh 'minikube service list' 
            }


        }
    
    
    
    
    
    
    
    
    
    
    
    }


}