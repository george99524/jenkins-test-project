pipeline {
    agent any

	environment {
		ENVIRONMENT = "PROD"
	}

    stages {
        stage('Checkout') {
            steps {
                sh 'ls -a'
                echo 'Checking out the main repository'
				checkout([$class: 'GitSCM',
						  branches: [[name: '*/master']],
					 userRemoteConfigs: [[url: 'https://github.com/george99524/jenkins-test-project.git']]])
                sh 'ls -a'
            }
        }
        stage('Finished') {
            steps {
                sh 'ls -a'
                echo 'finished'
            }
        }
    }
}
