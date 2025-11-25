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

        stage('Test Docker Inside Jenkins pipeline') {
            agent any  // Utilise un agent any pour exécuter des commandes Docker
            steps {
                sh 'docker ps'
                sh 'docker run --rm node:25-alpine node -v'
            }
        }

    
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
