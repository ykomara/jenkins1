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
            steps {
                echo "Building branch: ${params.BRANCH_NAME}"
                echo "Custom Text: ${params.CUSTOM_TEXT}"
                echo "Running Tests: ${params.RUN_TESTS}"
                echo "Deploying to environment: ${params.ENVIRONMENT}"
                script {
                    // Mask the secret key before printing (Jenkins also masks password parameters in console)
                    def masked = (params.SECRET_KEY ?: '').replaceAll(/./, '*')
                    echo "Using Secret Key: ${masked}"
                }
            }
        }
    }
}
