node{
  def branchM = 'quickstart-repository'
  def branchD = '*/ci-cd_develop'  
  def changeId
   
  stage('Configurar usuario') {
      script {  env.GIT_AUTHOR_EMAIL = 'abonilla@ultracom.com.co'
                env.GIT_AUTHOR_NAME = 'Abonilla-ultracom'}            
        
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: branchM]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('Cambios desde la rama de desarrollo') {
            
    checkout([$class: 'GitSCM', branches: [[name: branchD]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git', credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
    }
  stage('Migrar cambios a la rama de producción') {
            
                //checkout([$class: 'GitSCM', branch: [[name: branchM]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git', credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27']]])
                //sh 'git merge '+branchD
           
    //}
  }
}
//node {
//    stage('Conexión GCP') {
//        withCredentials([string(credentialsId: 'poc-ci-cd-375313', variable: 'GCP_CRED')]) {
//            sh 'gcloud auth activate-service-account --key-file ${GCP_CRED}'
//            sh 'gcloud config set project <poc-ci-cd-375313>'
//        }
//    }
//    stage('Dataform') {
//        sh 'dataform init --project <poc-ci-cd-375313>'
//        sh 'dataform push --push-all --env production'
 //   }
//    stage('Despliegue') {
//        sh 'dataform deploy --env production'
//    }
//}
// prueba Juan
}