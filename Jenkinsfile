pipeline {
    agent {
        docker {
            image 'node:25-alpine'
        }
    }

    options {
        timeout(time: 1, unit: 'HOURS') // permet de limiter le temps d'exécution du pipeline
    }

    stages {

        options {
            timestamps() //ajoute l'heure à chaque ligne de log
        }

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
