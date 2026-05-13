pipeline {
agent any
stages {
stage('Clone') {
    steps {
        git branch: 'main',
            url: 'https://github.com/tushardk058/ci-node-app.git'
    }
}
stage('Install') {
steps {
bat 'npm install'
}
}
stage('Run App') {
steps {
bat 'node app.js'
}
}
stage('Test') {
steps {
bat 'npm test'
}
}
}
}