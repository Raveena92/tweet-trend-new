pipeline {
    agent {
        label 'maven'
    }

    stages {
        stage('build') {
            steps {
                mvn clean package
            }
        }
    }

    stages {
        stage('SonarQube Analysis') {
             steps {
                withSonarQubeEnv('sonarqube-server') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
