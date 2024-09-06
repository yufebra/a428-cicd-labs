node {
    def mvnHome
    docker {
        image 'node:16-buster-slim'
        args '-p 3000:3000'
    }
    stage('Preparation') {
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
        mvnHome = tool 'M3'
    }
    stage('Build') {
        script {
            sh 'npm install'
        }
    }

    stage('Test') {
        script {
            sh './jenkins/scripts/test.sh'
        }
    }
}