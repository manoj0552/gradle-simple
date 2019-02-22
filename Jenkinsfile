#!/usr/bin/groovy

string branchName

if(!env.BRANCH_NAME){
    branchName = 'master'        
}
else{
    branchName = env.branchName    
}

library identifier: "SharedLibrary@master",
		retriever: modrenSCM([ 
		$class: 'GitSCMSource',
		remote: 'https://github.com/manoj0552/gradle-simple.git'	
	 ])
	 
	 pipeline {
 	    stages {
    	     stage('checkout') {
    	     
     	    checkout([
            $class: 'GitSCM',
            branches: scm.branches,
            extensions: scm.extensions + [[$class: 'LocalBranch'], [$class: 'WipeWorkspace']],
            userRemoteConfigs: [[credentialsId: 'Manoj2', url: 'https://github.com/manoj0552/gradle-simple.git']],
            doGenerateSubmoduleConfigurations: false
        ])

     	    }

    	 }

 	}

	 
	









