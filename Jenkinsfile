pipeline {
    agent any
    stages {
//            stage('Clone repository') {
//            steps { 
 //                 checkout([$class:'GitSCM',
  //                branches: [[name: '*/main']],
  //                userRemoteConfigs: [[url: 'https://github.com/Bindugowda2004/PES1UG23CS840_Jenkins.']]])
  //            }
   //         }
                
        stage('Build') {
            steps {
                  build 'PES1UG23CS840-1'
                  sh 'g++ main.cpp -o output'
                
            }
        }
        stage('Test') {
            steps {
              
                    sh './output'  
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
