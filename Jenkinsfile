pipeline {
   agent any

   stages {
      stage('checkout') {
         steps {
             checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'gitid', url: 'https://github.com/sudhfree/testrepo2.git']]])
         }
      }
      
      stage("list the files")
      {
          steps{
          bat label: '', script: 'dir'
          }
      }
   }
}
