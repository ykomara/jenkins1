pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                echo "Build !"
            }
        }

        stage('Deploy') {

            input {
                message "Ready to deploy. Proceed?"
                ok "Deploy"
                submitter "admin,devops"
                submitterParameter "USER_SUBMITTER" // capture the user who approved the deployment

                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'la version à déployer')
                }
            }

            steps {
                echo "user: ${USER_SUBMITTER}"
                echo "Version: ${VERSION}"
                echo "Deploy !"
            }
        }
    }
}
