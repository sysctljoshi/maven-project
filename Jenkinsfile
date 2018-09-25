pipeline {
    agent any
    
    stages{
        stage('Build'){
         steps{
             def mvn_version = 'M3'
            withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] )
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