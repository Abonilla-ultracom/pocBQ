
node{
  
  def branchD = '*/ci-cd_develop'  
  
   
  stage('Configurar usuario') {
      script {  env.GIT_AUTHOR_EMAIL = 'abonilla@ultracom.com.co'
                env.GIT_AUTHOR_NAME = 'Abonilla-ultracom'}            
        
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: branchD]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('Cambios desde la rama de desarrollo') {
            
    checkout([$class: 'GitSCM', branches: [[name: branchD]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git', credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
    sh 'git commit -m "Actualizando a la última versión"'
    }
  
  //stage('Procesar cambios') {
  // Hacemos el commit de los cambios
  //sh 'git commit -m "Actualizando a la última versión"'
  // Generamos un pull request a producción
  //sh 'git push origin develop:production'
  
  stage('Migrar cambios a la rama de producción') {
            
                //checkout([$class: 'GitSCM', branch: [[name: branchM]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git', credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
                //sh 'git merge '+branchD
           
  }
 }
}


