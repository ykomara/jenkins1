pipeline {
    agent any  

    triggers {
        cron('* * * * *') // vérifier les modifications chaque minute
    }
    

    stages {
        stage('Build') {
            steps {
                echo "Build !"
            }
        }
    }
}
