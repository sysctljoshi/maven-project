pipeline {
    agent any

    tools{
    maven 'maven 3'
     }
    
    stages{
        stage('Build'){
         steps{
             sh 'mvn clean package'
         }
         post {
             success {
                 echo 'now Archiving'
                 archiveArtifacts artifacts: '**/target/*.war'
             }
         }
        }
    }
}