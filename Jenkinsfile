pipeline {
    agent any 
    stages{
        stage('Stage 1'){
            steps{
                echo 'Hello world'
            }
        }
    }

    /*stages{
        stage('Build'){
            steps{
                echo 'Cleaning...'
                withMaven {
                    sh 'mvn clean'
                }
                
                echo 'Cleaned'
                echo 'Packaging...'
                
                withMaven {
                    sh 'mvn package'
                }
                
                echo 'Packaged'
            }

            post{
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: 
                    //target/*.war'
                    echo 'Archived'
                }
            }
        }
    }*/
}