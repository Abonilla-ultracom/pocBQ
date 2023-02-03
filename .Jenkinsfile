Jenkinsfile (Declarative Pipeline)
node{
  def ci-cd_develop = 'quickstart-repository'  
  def changeId
  stage('checkout'){
    checkout([$class: 'GitSCM', ci-cd_developes: [[name: ci-cd_develop]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'jenkinsCreds', url: 'https://github.com/miUsuario/miRepositorio.git']]])
  }
  stage('pull changes'){
    sh 'git pull origin '+ ci-cd_develop
  }
  stage('merge changes'){
    sh 'git merge origin development'
  }
  stage('push changes'){
    sh 'git push origin '+ ci-cd_develop
    changeId = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
  }
  stage('approve changes'){
    input message: 'Aprobar cambios?', ok: 'Aprobar'
  }
  stage('test'){
    sh 'mvn clean test'