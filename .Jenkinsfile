node{
   
  def branch = 'quickstart-repository'  
  def changeId
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: branch]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('Cambios desde la rama de desarrollo') {
            
    checkout([$class: 'GitSCM', branches: [[name: '*/ci-cd_develop']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
    }
  stage('Migrar cambios a la rama de producción') {
            
                checkout([$class: 'GitSCM', branches: [[name: 'quickstart-repository']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
                sh 'git merge origin/ci-cd_develop'
           
    }
}  
