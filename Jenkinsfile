pipeline {
    agent any

    environment {
        IMAGE_NAME = "adijawanjal/swiggy:latest"
        CONTAINER_NAME = "swiggy-app"
    }

    stages {
        stage('Pull Docker Image') {
            steps {
                sh 'docker pull $IMAGE_NAME'
            }
        }

        stage('Remove Existing Container') {
            steps {
                sh 'docker rm -f $CONTAINER_NAME || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d --name $CONTAINER_NAME -p 8080:80 $IMAGE_NAME'
            }
        }
    }

    post {
        success {
            echo "✅ Deployment completed successfully!"
        }
        failure {
            echo "❌ Deployment failed."
        }
    }
}

