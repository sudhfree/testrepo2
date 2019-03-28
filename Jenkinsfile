node {
    
    stage("Checkout code from github") {
        
        echo "Checking out code from master"
        
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/sudhfree/testrepo2.git']]])
        
    }
    
     stage("displaying the content") {
        
       
       bat 'dir'
        
    }
    
     stage("stage 3") {
        
        echo "this is stage 3"
        
    }
    
}