pipeline {
    agent any  

    stages {
        stage ('Build') {
            steps {
                sh 'echo hello > world.txt'
                archiveArtifacts(artifacts: '**/*.txt', fingerprint: true)
            }

        }

        
    }
}
