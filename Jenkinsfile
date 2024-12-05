pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/sunny-zhaoyishan/task1.git'
            }
        }
        stage('Build') {
            steps {
                // 执行构建步骤，例如使用Maven或Gradle构建项目
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // 执行测试步骤，例如运行JUnit测试
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // 执行部署步骤，例如将应用部署到服务器
                sh 'scp target/your-app.jar user@server:/path/to/deploy/'
            }
        }
    }
}
