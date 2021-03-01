pipeline{
    agent any

    parameters {
        string(name: 'DOCKER_IMAGE_NAME', defaultValue: 'image_name', description: 'Docker image name')
    }

    stages{
        stage('docker build'){
            steps{
                sh "docker build -t ${DOCKER_IMAGE_NAME} ."
            }
        }
    }
}