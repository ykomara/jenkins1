pipeline {
    agent {
        docker {
            image 'node:25-alpine'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
