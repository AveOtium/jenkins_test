pipeline {
agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/AveOtium/jenkins_test',
                        name: 'origin'
                    ]]
                ])
            }
        }
        stage('Install') {
            steps {
                bat 'C:\\Users\\ilay2\\AppData\\Local\\Microsoft\\WindowsApps\\python -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}