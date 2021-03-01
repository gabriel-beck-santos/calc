pipeline {
    agent any
    
    parameters { 
        string(name: 'DOCKER_IMAGE_NAME', defaultValue: 'calc', description: 'Adicionar um nome a imagem docker')
        string(name: 'DOCKER_CONTAINER_NAME', defaultValue: 'calc', description: 'Adicionar um nome do container')
    }
    stages {
        stage ('Build Docker Image') {
                agent any
                steps {
                        sh "docker build -t ${DOCKER_IMAGE_NAME} ."
                }
        }
        stage ('CleanResources') {
            agent any
            steps{
                cleanWs()
            }
        }
    }
}