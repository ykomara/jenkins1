pipeline {
    agent any  // exécute sur Jenkins (beaucoup plus rapide)
    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        text(name: 'CUSTOM_TEXT', defaultValue: 'Hello, Jenkins!', description: 'Custom text input')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests after build')
        choice(name: 'ENVIRONMENT', choices: ['development', 'staging', 'production'], description: 'Select the deployment environment')
        password(name: 'SECRET_KEY', defaultValue: '', description: 'Enter your secret key')
    }

    stages {
        stage('Build') {
            echo "Building branch: ${BRANCH_NAME}"
            echo "Custom Text: ${CUSTOM_TEXT}"
            echo " Running Tests: ${RUN_TESTS}"
            echo "Deploying to environment: ${ENVIRONMENT}"
            echo "Using Secret Key: ${SECRET_KEY.replaceAll(/./, '*')}" // Mask the secret key
            
        }
    }
}
