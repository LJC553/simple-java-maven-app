pipeline {
    agent any
    tools {
        maven 'Maven_3.8.5' // Jenkins中配置的工具
    }
    stage('Check Maven') {
    steps {
        bat 'where mvn'
        bat 'mvn -v'
    }
}
    stage('Print Env') {
    steps {
        bat 'set'
    }
}
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package -DskipTests'
            }
        }
    }
}
