pipeline {
    agent any

    environment {
        APP_NAME = 'hello-world-app'
        DEPLOY_DIR = '/tmp/deploy'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                git branch: 'main', url: 'https://github.com/<your-username>/<your-repo>.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Simulate a build step (replace with real build commands)
                sh 'echo "Compiling source code..."'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Simulate test step (replace with real test commands)
                sh 'echo "All tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Simulate deployment (replace with real deployment commands)
                sh """
                mkdir -p ${DEPLOY_DIR}
                echo "Hello World App deployed at $(date)" > ${DEPLOY_DIR}/app.txt
                """
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
