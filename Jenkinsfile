pipeline {
	 agent any
	 stages {
	 	stage('setup'){
			steps {
			      sh(script: 'pip install pytest')
			      }
		}
		stage('Testing'){
			steps {
			      sh(script: 'py.test --junitxml results.xml tests.py')
			      }
		}
	}
	post {
	     always {
	     	    junit(testResults: 'results.xml', allowEmptyResults : true)
		    }
		    
    	     }
}


