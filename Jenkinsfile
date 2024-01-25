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
                script {
                    sh "mvn clean install"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh "mvn test"
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
