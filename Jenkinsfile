pipeline {
    agent any
    stages {
//         stage('Clone repository') {
//             steps {
//                 checkout([$class: 'GitSCM', 
//                 branches: [[name: '*/main']], 
//                 userRemoteConfigs: [[url: 'https://github.com/rashmisomu/PES2UG21CS442_Jenkins.git']]])
//             }
//         }
        stage('Build') {
            steps {
                build 'PES2UG21CS442-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
               sh 'deploy_script.sh --invalid-option'
    }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
