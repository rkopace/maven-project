pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'Maven clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}