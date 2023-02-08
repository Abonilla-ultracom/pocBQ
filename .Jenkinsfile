node{
  
  def branchD = '*/ci-cd_develop'
  //def branchM = '*/quickstart-repository'  
    
  //stage('Configurar usuario') {
  //    script {  env.GIT_AUTHOR_EMAIL = 'abonilla@ultracom.com.co'
  //              env.GIT_AUTHOR_NAME = 'Abonilla-ultracom'}            
        
  stage('checkout'){
  checkout([$class: 'GitSCM', branches: [[name: branchD]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('Cambios desde la rama de desarrollo') {     
  checkout([$class: 'GitSCM', branches: [[name: branchD]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git', credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
  }
  
  stage('Procesar cambios') {
  // Hacemos el commit de los cambios
  
  //git branch: 'ci-cd_develop', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git'
  //sh 'git push origin  ci-cd_develop' 
  //sh 'git checkout quickstart-repository'
  //sh 'git pull origin quickstart-repository'
  //sh 'git checkout quickstart-repository'
  //sh 'git merge ci-cd_develop'
  //sh 'git push -u origin quickstart-repository'
  //sh 'git pull --rebase origin quickstart-repository'
  //sh 'git push origin  quickstart-repository'
  //sh 'git request-pull ci-cd_develop https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git quickstart-repository'
  //sh 'git merge ci-cd_develop'

  }
  stage('Procesar cambios dev') {
  
  //git branch: 'ci-cd_develop', 
  url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git'
  sh 'git pull origin ci-cd_develop'
  sh 'git push origin  ci-cd_develop' 
  //sh 'git checkout quickstart-repository'
  //sh 'git pull origin quickstart-repository'
  //sh 'git checkout quickstart-repository'
  //sh 'git merge ci-cd_develop'
  //sh 'git push -u origin quickstart-repository'
  //sh 'git pull --rebase origin quickstart-repository'
  //sh 'git push origin  quickstart-repository'
  //sh 'git request-pull ci-cd_develop https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git quickstart-repository'
  //sh 'git merge ci-cd_develop'

  }
}




