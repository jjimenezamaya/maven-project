pipeline {
    agent any  
    stages{
        stage('Build'){
            steps {
                git url: 'https://github.com/jjimenezamaya/maven-project'
                echo 'Cleaning and packaging with maven...'

                withMaven {
                    sh 'mvn clean package'
                }
            }

            post{
                success{
                    echo 'DONE'
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                    echo 'Archived'
                }

                failure {
                    echo 'FAILED'
                }
            }
        }
    }
}