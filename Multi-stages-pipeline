pipeline {
   agent any
    options {

    buildDiscarder(
        logRotator(
            // number of build logs to keep
            numToKeepStr:'5',
            // history to keep in days
            daysToKeepStr: '15',
            // artifacts are kept for days
            artifactDaysToKeepStr: '15',
            // number of builds have their artifacts kept
            artifactNumToKeepStr: '5'
        )
    )
    disableConcurrentBuilds()
    timestamps()
}

    stages {
      
        stage('ONGCBuild'){
            steps {
                cleanWs()
                echo 'Building the ongc application'
                sh 'mkdir ONGCBuild'
                echo 'sucess on ONGC Build'
            }
        }
        stage('ONGCTEST') {
            steps {
                echo 'testing the ongc applciation'
                sh 'mkdir ONGCTEST'
                echo 'sucess on ONGC test'
            }
        }
        stage('ONGCDeploy') {
            steps {
                echo 'deploying the ONGC Application'
                sh 'mkdir ONGCDeploy'
                echo 'sucess on ONGC Deploy'
            
                print BUILD_URL
                sh 'ls -lart'
                sh 'pwd'
                echo 'The Job is tringed from Options project'
            
            }

        }
    
    }
}
