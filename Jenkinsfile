pipeline {
agent any
stages {
stage('Clone') {
    steps {
        git branch: 'main',
            url: 'https://github.com/tushardk058/ci-node-app.git'
    }
}
    stages {

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'node app.js'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
}