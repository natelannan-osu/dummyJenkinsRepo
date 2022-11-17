pipeline {
	 agent any
	 stages {
	 	stage('setup'){
			steps {
			      sh(script: 'pip3 install pytest')
			      sh(script: 'python -m pytest test.py')
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


