pipeline {
    agent {
        label 'localhost'
    }
    environment {
        envString = 'true'
    }
    post {
        always {
            bat "echo always"
        }
        failure {
            bat "echo failure"
        }
        success {
            bat "echo success"
        }
    }
    stages {
    
        stage("Этап"){
            steps{
                bat "echo сообщение из этапа"
                bat "echo переменая envString ${envString}"
                script{
                    scannerHome - tool "sonar-scaner"
                }
            }
        }

    }
}