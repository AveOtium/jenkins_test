pipeline {
agent any
    stages {
        // stage('Checkout') {
        //     steps {
        //         checkout([
        //             $class: 'GitSCM',
        //             branches: [[name: '*/main']],
        //             userRemoteConfigs: [[
        //                 url: 'https://github.com/AveOtium/jenkins_test',
        //                 name: 'origin'
        //             ]]
        //         ])
        //     }
        // }
        stage('Checkout') {
            steps {
                git url:'<URL>', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                bat 'C:\\Users\\ilay2\\AppData\\Local\\Programs\\Python\\Python313\\python -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\\ilay2\\AppData\\Local\\Programs\\Python\\Python313\\python -m pytest'
            }
        }
    }
}