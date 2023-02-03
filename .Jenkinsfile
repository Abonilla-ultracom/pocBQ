node{
  def branch = 'quickstart-repository'  
  def changeId
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: branch]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://Abonilla-ultracom:1030Alvaro@github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('pull changes'){
    sh 'git pull origin '+branch
  }
  stage('merge changes'){
    sh 'git merge origin ci-cd_develop'
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
