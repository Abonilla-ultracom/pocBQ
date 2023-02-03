node{
  def branch = 'quickstart-repository'  
  def changeId
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: branch]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'jenkinsCreds', url: 'https://github.com/miUsuario/miRepositorio.git']]])
  }
  stage('pull changes'){
    sh 'git pull origin '+branch
  }
  stage('merge changes'){
    sh 'git merge origin development'
  }
  stage('push changes'){
    sh 'git push origin '+branch
    changeId = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
  }
  stage('approve changes'){
    input message: 'Aprobar cambios?', ok: 'Aprobar'
  }
  stage('test'){
    sh 'mvn clean test'
  } 
}  
