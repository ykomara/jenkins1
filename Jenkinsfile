pipeline {
    agent any  
    parameters {
        booleanParam(name: 'DEPLOY_TO_PROD', defaultValue: false, description: ' Deploy to production?')   
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
                    equals expected: true, actual: params.DEPLOY_TO_PROD
                }
            }

            steps {
                echo "Deploy !"
            }
        }
    }
}
