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
 branch_name = scm.branches[0].name
artifact_home = System.getProperty("user.home")
dir(artifact_home+"\\"+JOB_NAME+"\\"+branch_name.split("/")[1]+"\\"+BUILD_NUMBER)
{
    folder = artifact_home+"\\"+JOB_NAME+"\\"+branch_name.split("/")[1]+"\\"+BUILD_NUMBER
    if(!fileExists('/'))
    {
       bat "mkdir ${folder}"
        bat "dir ${artifact_home}"
       println(scm.branches[0].name)
    }
}
}

}
