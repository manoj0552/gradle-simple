pipeline {
    agent any
	stages {
	    stage('checkout') {
	    
	    git credentialsId: 'fbd8b275-22c9-4cb1-8645-7f9d51e92fee', 
	    url: 'https://github.com/manoj0552/gradle-simple.git'
	    branch: 'master'
    	   
    	}
    
	}
	stages {
	    stage('sonar') {
	    
	    sh 'gradle sonarqube'
    	   
    	}

	}


}
