pipeline {
    agent any
	stages {
	    stage('checkout') {
	    	steps {
	    
	    git credentialsId: 'Manoj2', url: 'https://github.com/manoj0552/gradle-simple.git'
    	    
    	}	        	   
    	}
    	 stage('sonar') {
    	 steps {
    	    	 
    	  bat 'gradle build sonarqube'
    	  
 	        
 	    }
	   
    	   
    	}
    
	}
}
