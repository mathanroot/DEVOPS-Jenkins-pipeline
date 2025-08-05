pipeline {
    agent any

    environment {
        IMAGE_NAME = 'js-app'
        DOCKER_HUB_USER = 'mathan003' 
    }

    stages {
        stage('Clone Repo') {
            steps {
                echo "Cloning the repository..."
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Building Docker image..."
                script {
                    docker.build("${IMAGE_NAME}")
                }
            }
        }

        stage('Run Tests') {
            steps {
                echo "Running tests (placeholder)..."
                
                sh 'echo "Tests passed!"'
            }
        }

        stage('Push to DockerHub') {
            steps {
                echo "Pushing image to DockerHub..."
                withCredentials([usernamePassword(credentialsId: 'dockerhub-creds', usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                    sh """
                        echo "$PASS" | docker login -u "$USER" --password-stdin
                        docker tag ${IMAGE_NAME} ${DOCKER_HUB_USER}/${IMAGE_NAME}:latest
                        docker push ${DOCKER_HUB_USER}/${IMAGE_NAME}:latest
                    """
                }
            }
        }

        stage('Deploy App') {
            steps {
                echo "Deploying the app (placeholder)..."
                
                sh 'echo "App deployed!"'
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
