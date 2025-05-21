pipeline {
    agent any
    stages {
        stage('Welcome') { 
            steps {
                echo 'Hi , You are inside the pipeline'
            }
        }
        stage('build') {
            steps {
                script {
                    docker.build('hello-world-app')
                }
            }
        stage('Push DockerImage') {
            steps {
               sh 'docker tag hello-world-app gayatridevops11/pythonapp:latest'
               sh 'docker push gayatridevops11/pythonapp:latest'
            }
        }
        }
    }
}
