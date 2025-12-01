pipeline {
    agent any  

    stages {
        stage ('Build') {
            steps {
                echo 'Sent email test'
            }

            post {
                success{
                    emailext ( 
                    to: 'yayakomara56@gmail.com', 
                    body: 'Build started.',
                    subject: 'Build Notification'
                )
                }
            }

        }
    }
}
