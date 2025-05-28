pipeline {
    agent any
    tools {
        maven 'Maven_3.8.5' // Jenkins中配置的工具
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }
    }
}
