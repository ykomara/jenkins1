pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                echo "Build !"
            }
        }

        stage('Deploy') {

            when {
                branch 'main'
            }

            steps {
                echo "Deploy !"
            }
        }
    }
}
