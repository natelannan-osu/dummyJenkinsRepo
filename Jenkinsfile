pipeline {
	 agent any
	 stages {
	 	stage('setup'){
			steps {
			      sh(script: 'pip3 install pytest')
			      }
		}
		stage('Testing'){
			steps {
			      sh(script: 'pytest --junitxml results.xml tests.py')
			      }
		}
	}
	post {
	     always {
	     	    junit(testResults: 'results.xml', allowEmptyResults : true)
		    }
		    
    	     }
}


