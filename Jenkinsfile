pipeline {
    agent none
	
	stages{
	
    stage("Checkout code from github") {
        steps{
        echo "Checking out code from master"
        
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/sudhfree/testrepo2.git']]])
        }
    }
    
     stage("displaying the content") {
        
       steps{
       bat 'dir'
        }
    }
    
     stage("stage 3") {
        
		steps{
        echo "this is stage 3"
      }  
    }
	}
    
}