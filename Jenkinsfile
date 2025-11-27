pipeline {
    agent any  

    environment {
        DEPLOY_ENV = "production" 
    }

    stages {
        stage('Build') {
            steps {
                echo "Build !"
            }
        }

        stage('Deploy') {


            when {
                allOf {
                    branch 'main'
                    environment name: 'DEPLOY_ENV', value: 'production' // only deploy to production if DEPLOY_ENV is set to 'production'
                }
            }

            steps {
                echo "Deploy !"
            }
        }
    }
}
