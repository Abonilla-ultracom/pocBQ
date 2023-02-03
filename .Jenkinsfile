pipeline {
    agent any
    stages {
        stage('Clonar el repositorio') {
            steps {
                git url: 'https://github.com/Abonilla-ultracom/pocBQ.git'
                checkout([$class: 'GitSCM', userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
            }
        }
        
    }
}