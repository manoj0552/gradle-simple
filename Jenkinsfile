pipeline {
    agent any
    options {
        skipDefaultCheckout(true)
    }

	stages {
	    stage('checkout') {
	    	steps {    	  
    
            checkout([$class: 'GitSCM', 
            branches: [[name: '*/master']], 
            doGenerateSubmoduleConfigurations: false, 
            extensions: [[$class: 'CleanBeforeCheckout']], 
            submoduleCfg: [], 
            userRemoteConfigs: [[credentialsId: 'Manoj2',
                url: 'https://github.com/manoj0552/gradle-simple.git']]])
    	}	        	   
    	}
    	 stage('sonar') {
    	 steps {
    	    	 
    	  bat './gradlew ---debug clean build sonarqube'
    	  
 	        
 	    }
	   
    	   
    	}
    
	}
}
