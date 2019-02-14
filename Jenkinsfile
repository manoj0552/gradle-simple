pipeline {
    agent any
    options {
        skipDefaultCheckout(true)
    }

	stages {
	    stage('checkout') {
	    	steps {    	  
    
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/master' ]],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: scm.extensions + [[$class: 'SubmoduleOption', disableSubmodules: false, recursiveSubmodules: true, reference: '', trackingSubmodules: false]],
                    submoduleCfg: [],
                    userRemoteConfigs: [ credentialsId: 'Manoj2', 
                 url: 'https://github.com/manoj0552/gradle-simple.git']])
    	}	        	   
    	}
    	 stage('sonar') {
    	 steps {
    	    	 
    	  bat './gradlew build sonarqube'
    	  
 	        
 	    }
	   
    	   
    	}
    
	}
}
