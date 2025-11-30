pipeline {
    agent any  

    tools {
        gradle 'gradle9.4.0'
        nodejs 'nodejs25'
    }

    stages {
        stage ('Build') {
            steps {
                sh 'gradle -v'
                sh 'node -v'
                sh 'npm -v'
            }

        }

        
    }
}
