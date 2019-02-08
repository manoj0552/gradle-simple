pipeline {
    agent any
	stages {
	    stage('checkout') {
	    
	    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
	    doGenerateSubmoduleConfigurations: false, 
	    extensions: [], 
	    submoduleCfg: [], 
	    userRemoteConfigs: [[credentialsId: 'fbd8b275-22c9-4cb1-8645-7f9d51e92fee', 
	    url: 'https://github.com/manoj0552/gradle-simple.git']]])

	    
    	   
    	}
    
	}
	stages {
	    stage('sonar') {
	    
	    sh 'gradle sonarqube'
    	   
    	}

	}


}
