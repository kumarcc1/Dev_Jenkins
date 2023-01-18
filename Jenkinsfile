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
}
    parameters{
         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

//         text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

//         booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

//         choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        
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
        stage('ProjectNG'){
            steps{
                cleanWs()
                
                sh 'mkdir Slack'
                sh 'mkdir TEST'
                sh 'mkdir Deploy'
                sh "echo tool name is $PERSON"
                echo 'The assinged task completed on jenkins'
                print BUILD_URL
                
            }
        }
    } 
}    
