pipeline {
    agent any
    
    parameters{ 
        // Tem que se ir ao Jenkins > Configure > This project is parameterized. 
        string(name: 'DOCKER_IMAGE_NAME', defaultValue: 'image_name', description: 'Docker image name')

        string(name: 'DOCKER_CONTAINER_NAME', defaultValue: 'container_name', description: 'Docker container name')

        string(name: 'DOCKER_PORT', defaultValue: '3000', description: 'Docker port')
    }
    stages {
        stage ('Build Docker Image') {
                steps {
                        sh "docker build -t ${DOCKER_IMAGE_NAME} ."
                }
        }
        stage ('CleanResources') {
            steps{
                cleanWs()
            }
        }
    }
}