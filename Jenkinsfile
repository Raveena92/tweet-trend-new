pipeline {
    agent {
        label 'maven'
    }

    stages {
        stage('Debug') {
            steps {
                sh 'echo "Host: $(hostname)"'
                sh 'echo "User: $(whoami)"'
                sh 'echo "PATH: $PATH"'
                sh 'which mvn || true'
                sh 'mvn -version || true'
            }
        }
