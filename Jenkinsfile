pipeline {
    agent any  // exécute sur Jenkins (beaucoup plus rapide)

    stages {
        stage('Build') {
            agent {
                docker { image 'node:25-alpine' } // lance Docker SEULEMENT ici
            }
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('Test Docker Inside Jenkins pipeline') {
            agent any  // exécute sur Jenkins
            steps {
                sh 'docker ps'
            }
        }
    }
}
