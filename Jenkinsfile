pipeline {
    agent any

	 tools {
        maven 'MAVEN_HOME'
    }


    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    bat 'mvn clean package'
		    echo "Build Application"
                }
            }
        }

        stage('Deploy') {
            steps {
		   echo "Deploy Application"
            }
        }
	stage('Test') {
            steps {
                echo "Testing App"
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed!'
        }
    }
}
