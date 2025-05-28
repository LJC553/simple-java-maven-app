pipeline {
    agent any
    tools {
        maven 'maven381'  // 请确保你在 Jenkins 全局工具配置中配置了这个名
    }
    stages {
        stage('打印环境变量') {
            steps {
                bat 'set'
            }
        }
        stage('验证 Maven') {
            steps {
                bat 'where mvn'
                bat 'mvn -v'
            }
        }
        stage('构建') {
            steps {
                bat '''
                echo ===== 开始构建 =====
                mvn -B -DskipTests clean package
                echo ===== 构建完成 =====
                '''
            }
        }
    }
}
