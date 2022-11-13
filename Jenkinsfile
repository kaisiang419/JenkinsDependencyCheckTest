pipeline {
	agent any
	stages {
		stage('OWASP DependencyCheck') {
			steps {
				dependencyCheck additionalArguments: '--format HTML --format XML', odcInstallation: 'OWASP-check-730'
			}
		}
	}	
	post {
		success {
			dependencyCheck additionalArguments: 'dependency-check-report.xml', odcInstallation: 'OWASP-check-730'
		}
	}
}
