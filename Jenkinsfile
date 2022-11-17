pipeline {
	 agent any
	 stages {
	 	stage('Hello'){
			steps {
			      echo 'Hello World'
			      }
		}
		stage('Testing'){
			steps {
			      sh(script: 'python -m pytest --junitxml results.xml tests.py')
			      sh(script: 'pwd')
			      }
		}
	}
	post {
	     always {
	     	    echo 'Error?'
	     	    junit(testResults: 'results.xml', allowEmptyResults : true)
		    }
		    
    	     }
}


