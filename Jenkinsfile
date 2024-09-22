pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('myapp:latest')
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Add steps to run tests, e.g., using PyTest for Python bots
                }
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    kubernetesDeploy(
                        configs: 'path-to-deployment.yaml',
                        kubeconfigId: 'your-kubeconfig-credentials-id'
                    )
                }
            }
        }
    }
}
