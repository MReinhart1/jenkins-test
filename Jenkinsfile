pipeline {
    agent any

    environment {
        NAME = "Michael"
        secret = credentials('TEST')
        registryCredential = 'dockerhub_id' 
        registry = "michaelreinhart112/web1" 

    }

    stages {
        stage('Build') {
            steps {
                node --version
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Push') {
            steps {
                echo "Pushing up image"
            }
            
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo "I willl always be executed"
        }
        success {
            echo "This worked"
        }
        failure {
            echo "This did not work"
        }
    }
}
