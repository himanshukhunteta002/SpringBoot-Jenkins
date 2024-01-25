pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn clean install"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    def mvnHome = tool 'Maven'
                    sh "${mvnHome}/bin/mvn test"
                }
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
