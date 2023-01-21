pipeline {
    agent {
        label 'maven'
    }
    stages {
        stage("parallel") {
            parallel{
                stage('ProjectNG'){
                    steps {
                        sh 'touch file{1..10}'
                        sh 'ls -lart && pwd'
                    }
                }
                stage('ProjectONGC'){
                    steps{
                        sh 'touch file{10..20}'
                        sh 'ls -lart && pwd'
                    }
                }
            }
        }
        stage('ProjectONGC'){
            steps{
                script{
                    sh 'mkdir ONGCParallel'
                dir('ONGCParallel'){
                      try{
                        sh 'mkdir devopstest'
                        sh "echo hello > a"
                        sh 'cat a'
                        }catch (Exception e){
                            echo 'folder already exist'
                        }
                }
       
                
                sh 'ls -lart & pwd'
                sh 'cat /etc/passwd'
            }
        }
    }
}
