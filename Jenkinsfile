pipeline {
    // 在任何一个可用的 Jenkins Agent 上执行
    agent any

    stages {
        // 第一阶段：简单的打招呼
        stage('Hello') {
            steps {
                echo 'Hello World!'
                echo '这是我的第一个 Jenkins 流水线'
            }
        }
        
        // 第二阶段：显示一些系统信息
        stage('系统信息') {
            steps {
                sh 'uname -a'      // 显示系统信息（Linux/Mac）
                // 如果是 Windows，用 bat 'systeminfo'
                sh 'whoami'        // 显示当前用户
                sh 'pwd'           // 显示当前工作目录
            }
        }
        
        // 第三阶段：展示环境变量
        stage('环境变量') {
            steps {
                echo "构建编号: ${env.BUILD_ID}"
                echo "任务名称: ${env.JOB_NAME}"
                echo "构建URL: ${env.BUILD_URL}"
                echo "工作空间: ${env.WORKSPACE}"
            }
        }
    }
}

