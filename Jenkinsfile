pipeline {
    agent any

    parameters {
        choice(
            name: 'IMAGE_TAG',
            choices: ['1.0', '1.1', '1.2'],
            description: 'Select image version'
        )

        choice(
            name: 'ENVIRONMENT',
            choices: ['DEV', 'QA', 'UAT', 'PROD'],
            description: 'Select environment'
        )
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Docker Build') {
            steps {
                echo "Docker Build"
            }
        }

        stage('ECR Login') {
            steps {
                echo "ECR Login"
            }
        }

        stage('Push to ECR') {
            steps {
                echo "Push to ECR"
            }
        }

        stage('Select Image Tag') {
            steps {
                echo "Selected image: ${params.IMAGE_TAG}"
            }
        }

        stage('Deploy to Environment') {
            steps {
                echo "Deploying ${params.IMAGE_TAG} to ${params.ENVIRONMENT}"
            }
        }
    }
}
