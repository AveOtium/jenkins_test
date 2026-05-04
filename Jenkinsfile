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
        stage('Debug') {
            steps {
                bat 'where python'
                bat 'C:\\Users\\ilay2\\AppData\\Local\\Microsoft\\WindowsApps\\python3.exe --version'
                //bat 'python --version'
            }
        }
    //     stage('Install') {
    //         steps {
    //             bat 'python -m pip install -r requirements.txt'
    //         }
    //     }
    //     stage('Test') {
    //         steps {
    //             bat 'pytest'
    //         }
    //     }
    }
}