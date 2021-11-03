pipeline {
    agent any 
        
    stages{
        stage('Build'){
            steps{
                echo 'Cleaning...'
                sh 'mvn clean'
                echo 'Cleaned'
                echo 'Packaging...'
                sh 'mvn package'
                echo 'Packaged'
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