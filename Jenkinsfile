pipeline {
    agent any
    

    stages {
        stage('Hello') {
            steps {
                echo 'Reminder for EDGE->DEVEL Promotion'
            }
        }
    }
    post{
        always{
            emailext body: 'Reminder for EDGE->DEVEL Promotion', subject: 'Reminder for EDGE->DEVEL Promotion', to: 'abhijeetjain47@gmail.com'
        }
    }
}
