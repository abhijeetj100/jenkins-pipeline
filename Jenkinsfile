pipeline {
    agent any
    

    stages {
        stage('Hello') {
            steps {
                echo 'Reminder for QA->PROD & DEVEL->QA Promotion'
            }
        }
    }
    post{
        always{
            emailext body: 'Reminder for QA->PROD & DEVEL->QA Promotion', subject: 'Reminder for QA->PROD & DEVEL->QA Promotion', to: 'abhijeetjain47@gmail.com'
        }
    }
}
