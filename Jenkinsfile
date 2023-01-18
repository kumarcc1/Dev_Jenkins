pipeline {
    agent any
    environment{
        env = "UAT"
    }
    triggers{
        pollSCM('* * * * *')
    }

options {
disableConcurrentBuilds()
timestamps()
 buildDiscarder(logRotator(numToKeepStr: '3', daysToKeepStr: '1'))
}
//     options {

//     buildDiscarder(
//         logRotator(
//             // number of build logs to keep
//             numToKeepStr:'5',
//             // history to keep in days
//             daysToKeepStr: '15',
//             // artifacts are kept for days
//             artifactDaysToKeepStr: '15',
//             // number of builds have their artifacts kept
//             artifactNumToKeepStr: '5'
//         )
//     )
// }
    
       stages {
        stage('This NG Projectt'){
            steps{
                cleanWs()
                sh 'mkdir $Choice'
                sh 'mkdir Slack'
                sh 'mkdir TEST'
                sh 'mkdir Deploy'
                sh "echo tool name is $tool"
                echo 'The assinged task completed on jenkins'
                print BUILD_URL
                
            }
        }
    } 
}    
