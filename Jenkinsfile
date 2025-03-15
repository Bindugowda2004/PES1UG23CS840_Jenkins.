     pipeline {
         agent any
         stages {
             stage('Build') {
                 steps {
                     sh 'g++ -o hello_exec hello.cpp'
                 }
             }
             stage('Test') {
                 steps {
                     sh './hello_exec'
                 }
             }
             stage('Deploy') {
                 steps {
                     echo 'Deployment stage'
                 }
             }
         }
         post {
             failure {
                 echo 'Pipeline Failed'
             }
         }
     }
