pipeline {
    agent any  

    stages {

        stage('Build') {
            parallel (
                failFast: true,
                "Build frontend": {
                    echo "Build frontend !"
                },
                "Build backend": {
                    echo "Build backend !"
                }
            )
        }

        stage('Deploy') {
            steps {
                echo "Deploy !"
            }
        }
    }
}
