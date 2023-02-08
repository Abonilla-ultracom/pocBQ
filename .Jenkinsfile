pipeline {
    agent any
    stages {
      stage('Checkout') {
        steps {
          checkout([$class: 'GitSCM',
                    branches: [[name: '*/ci-cd_develop']],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: [],
                    submoduleCfg: [],
                    userRemoteConfigs: [[credentialsId:'0abb7957-5f3c-40b7-91d0-5f067e64be27',
                                        url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
        }
      }
      stage('Pull Request') {
        steps {
          sh 'git pull --rebase origin ci-cd_develop'
      //    sh 'git push origin ci-cd_develop'
          sh 'git request-pull ci-cd_develop HEAD:master'
      }
    }
  }
}
