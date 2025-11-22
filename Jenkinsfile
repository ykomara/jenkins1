pipeline {
    // Use any available agent
    agent {
        docker {
            image : 'node:25-alpine'
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
            echo 'This will always run after the stages finish'
        }
        success {
            echo 'This will run only if the pipeline succeeds'
        }
    }



}
