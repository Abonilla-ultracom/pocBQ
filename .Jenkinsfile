pipeline {
    agent any
    stages {
        stage('Clonar el repositorio') {
            steps {
                git 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git'
            }
        }
        stage('Cambios desde la rama de desarrollo') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/ci-cd_develop']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
            }
        }
        stage('Migrar cambios a la rama de producción') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'quickstart-repository']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
                sh 'git merge ci-cd_develop'
            }
        }
    }
}