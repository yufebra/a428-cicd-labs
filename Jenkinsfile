node {
    docker {
        image 'node:16-buster-slim'
        args '-p 3000:3000'
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