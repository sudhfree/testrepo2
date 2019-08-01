node
{
stage("checkout")
{
   checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a2b491cf-56da-4cfc-aec4-1acc493ee70e', url: 'https://github.com/sudhfree/testrepo2.git']]])
}
stage("check")
{
 bat 'dir'
}
 
}
