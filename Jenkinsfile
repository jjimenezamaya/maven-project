pipeline {
    agent any 
        
    stages{
        stage('Build'){
            steps{
                echo 'Starting with clean package command'
                sh 'mvn clean package'
                echo 'Cleaned and packaged'
            }

            post{
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                    echo 'Archived'
                }
            }
        }
    }
}