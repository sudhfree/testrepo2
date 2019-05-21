node
{
stage("checkout")
{
    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
    doGenerateSubmoduleConfigurations: false, extensions: [],
    submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GITHUBTRY',
    url: 'https://github.com/sudhfree/testrepo2.git']]])
}
stage("check")
{
 /*  dir() {
    // some block
    if(fileExists '/')
    {
        
    }
}*/
 println(scm.branches[0].name)
artifact_home = System.getProperty("user.home")
dir(artifact_home+env.BRANCH_NAME)
{
    folder = artifact_home+env.GIT_BRANCH
    if(!fileExists('/'))
    {
       bat "mkdir ${folder}"
       println(scm.branches[0].name)
    }
}
}

}
