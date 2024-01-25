pipeline {
    agent any

    
    tools {
    maven 'Maven'
    }


    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build App"
            }
        }

        stage('Test') {
            steps {
                echo "Testing App"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy App"
            }
        }
    }

    post {
        success {
            echo 'Build and test successful! Deploy your application.'
        }

        failure {
            echo 'Build or test failed! Check the logs for details.'
        }
    }
}
