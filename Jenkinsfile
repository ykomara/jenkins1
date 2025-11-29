pipeline {
    agent any  

    stages {
        stage('Build and Test') {
            matrix {
                axes {
                    axis {
                        name 'PLATFORM'
                        values 'Linux', 'MacOS', 'Windows'
                    }
                    axis {
                        name 'BROWSER'
                        values 'Firefox', 'Chrome', 'Safari'
                    }
                }

                stages {
                    stage('Build') {
                        steps {
                            echo "Building on ${PLATFORM} with ${BROWSER}"
                        }
                    }
                    stage('Test') {
                        steps {
                            echo "Testing on ${PLATFORM} with ${BROWSER}"
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
