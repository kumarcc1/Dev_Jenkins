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
                            sh 'mkdir Test'
                        } catch (Exception e){
                            echo 'the folder already exist'
                        }
                    }
                }
                sh 'ls -lart & pwd'
                sh 'cat /etc/passwd'
            }
        }
    }
}
