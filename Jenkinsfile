pipeline {
    agent any

    environment {
        DOCKER_REGISTRY = 'aliamin10'    // Your Docker Hub username
        IMAGE_NAME = 'webweather'       // Docker image name
        CONTAINER_NAME = 'weather-app'  // Docker container name
        DOCKER_PORT = '5000'            // Application port
    }

    stages {
        stage('Play Ansible') {
            steps {
                script {
                    // Assuming inventory and playbook.yml files are available
                    sh """
                        ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i inventory playbook.yml
                    """
                }
            }
        }
    }

}
