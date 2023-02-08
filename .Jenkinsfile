nodo{
  
  def branchD = '*/ci-cd_develop'
  def branchM = '*/repositorio de inicio rápido'  
    
  stage('Configurar usuario') {
      script { env.GIT_AUTHOR_EMAIL = 'abonilla@ultracom.com.co'
                env.GIT_AUTHOR_NAME = 'Abonilla-ultracom'}            
        
  etapa('pago'){
  checkout([$class: 'GitSCM', sucursales: [[nombre: branchD]], doGenerateSubmoduleConfigurations: false, extensiones: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27 ', URL: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('Cambios desde la rama de desarrollo') {     
  checkout([$class: 'GitSCM', sucursales: [[nombre: branchD]], doGenerateSubmoduleConfigurations: false, extensiones: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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 @github.com/Abonilla-ultracom/pocBQ.git', identificación de credenciales: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
  }
  
  stage('Procesar cambios') {
  // Hacemos el commit de los cambios
  
  rama git: 'ci-cd_develop', URL: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git'
  sh 'git push origen ci-cd_develop'
  sh 'git checkout repositorio de inicio rápido'
  sh 'git pull --rebase origen repositorio de inicio rápido'
  sh 'repositorio de inicio rápido de git push origen'
  sh 'git request-pull ci-cd_develop https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git quickstart-repository'
  //sh 'git fusionar ci-cd_develop'

  }
 }
}



