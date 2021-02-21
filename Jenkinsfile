pipeline {
    agent any
    def app
    stages {
        stage('Deploy') {
            steps {
                script {
                    app = docker.build 'ruggerii/jenkins-maven-jdk11'
                    docker.withRegistry('', 'ruggerii')
                    app.push('test')
                }
            }
        }
    }
}