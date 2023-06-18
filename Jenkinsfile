pipeline {
    agent any
    stages {
        stage('build-docker-image') {
            steps {
                build_docker_image()
            }
        }
      
    }
}

def build_docker_image(){
    echo "Building docker image.."
    sh "docker build --no-cache -t marcisvitols/api-tests . "
    
    echo "Pushing docker image to docker registry.."
    sh "docker push marcisvitols/api-tests"
}

