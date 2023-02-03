import jenkins.model.*
jenkins = Jenkins.instance

node{
  def branch = 'ci-cd_develop'  
  def changeId
  stage('checkout'){
    checkout([$class: 'GitSCM', branches: [[name: ci-cd_develop]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27', url: 'https://github.com/Abonilla-ultracom/pocBQ.git']]])
  }
  stage('pull changes'){
    sh 'git pull origin '+branch
  }
  stage('merge changes'){
    sh 'git merge origin'
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
