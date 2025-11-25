pipeline {
    agent {
        docker {
            image 'node:25-alpine'
        }
    }

    options {
        timeout(time: 1, unit: 'HOURS') // permet de limiter le temps d'exécution du pipeline
        timestamps() // ajoute des timestamps aux logs de la console
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
