pipeline {
    agent any

    tools {
        maven "M398"
    }

    stages {
        stage('Maven Version') {
            steps {
                sh 'mvn -version'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
