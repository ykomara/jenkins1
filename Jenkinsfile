pipeline {
    agent any  

    triggers {
        pollSCM('* * * * *') // vérifier les modifications chaque minute
    }
    

    stages {
        stage('Build') {
            steps {
                echo "Build !"
            }
        }
    }
}
