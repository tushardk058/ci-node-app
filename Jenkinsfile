pipeline {
agent any
stages {
stage('Clone') {
steps {
git 'https://github.com/tushardk058/ci-node-app.git'
}
}
stage('Install Dependencies') {
steps {
sh 'npm install'
}
}
stage('Run Application') {
steps {
sh 'node app.js'
}
}
stage('Run Tests') {
steps {
sh 'npm test'
}
}
stage('Build Docker Image') {
steps {
sh 'docker build -t ci-node-app .'
}
}
stage('Run Docker Container') {
steps {
sh 'docker run -d -p 3000:3000 --name ci-container ci-node-app'
}
}
}
}