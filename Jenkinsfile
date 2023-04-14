pipeline {
    agent any
    stages {
        stage ('Build Dockerfile') {
            steps {

               sh 'docker build -t sample_html .' 
            }


        }


        stage ('Docker run') {
            steps {

               sh 'docker run -p85:80 -d sample_html' 
            }


        }



    }


}