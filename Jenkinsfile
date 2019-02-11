pipeline {
    agent any
	stages {
	    stage('checkout') {
	    steps {
	    
	    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
	    doGenerateSubmoduleConfigurations: false, 
	    extensions: [], 
	    submoduleCfg: [], 
	    userRemoteConfigs: [[credentialsId: 'Manoj2', 
	    url: 'https://github.com/manoj0552/gradle-simple.git']]])
    	    
    	}	        	   
    	}
    	 stage('sonar') {
    	 steps {
    	    	 
    	  bat 'gradle build sonarqube'
    	  
 	        
 	    }
	   
    	   
    	}
    
	}
}
