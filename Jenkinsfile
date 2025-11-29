pipeline {
    agent any  

    options {
        parallelAlwaysFailFast()
    }

    stages {
        stage('Build') {
            parallel {
                stage('Build frontend') {
                    steps {
                        echo "Build frontend !"
                    }
                }

                stage('Build backend') {
                    steps {
                        echo "Build backend !"
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy !"
            }
        }
    }
}
