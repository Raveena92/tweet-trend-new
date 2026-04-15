pipeline {
    agent {
        label 'maven'
    }

    stages {
        stage('build') {
            steps {
               sh 'mvn clean package'
            }
        }
    }

        stage('SonarQube Analysis') {
             steps {
                withSonarQubeEnv('sonarqube-server') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    
}
