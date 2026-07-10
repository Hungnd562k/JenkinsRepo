pipeline {
    agent {
        docker { image 'node:24.18.0-alpine3.24' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --eval "console.log(process.platform,process.env.CI)"'
            }
        }
    }
}