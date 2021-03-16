pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World v2'
            }
        }
    }
    post{
        always{
            emailext body: 'Test email body', subject: 'Test Email', to: 'abhijeetjain47@gmail.com'
        }
    }
}
