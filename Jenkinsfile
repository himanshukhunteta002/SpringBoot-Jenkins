pipeline {
    agent any

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
                    sh 'mvn clean package'
					echo "Build Application"
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
					echo "Deploy Application"
                }
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
