pipeline {
    agent any
    tools {
    maven 'M3'
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