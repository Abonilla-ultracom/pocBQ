pipeline {

  def branchD = '*/ci-cd_develop'

    agent any
    stages {
        stage('Detect Development Branch') {
            steps {
                git branch: branchD ,
                url: 'https://Abonilla-ultracom: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@github.com/Abonilla-ultracom/pocBQ.git' , credentialsId: '0abb7957-5f3c-40b7-91d0-5f067e64be27',
                
                
            }
        }
        //stage('Generate Pull Request') {
          //  when {
             //   branch 'ci-cd_develop'
            //}
            //steps {
              //  script {
                //    git pull
                  //  git checkout -b dev
                    //git commit -a -m "Autogenerated pull request"
                    //git push origin ci-cd_develop
                //}
            //}
        //}
    }
}