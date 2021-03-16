pipeline {
    agent any
    
    parameters{
        string(name: 'DAY_ENV', defaultValue: '0', description: 'number denoting day in week, 1 - monday and 3 - wednesday') 
        
    }
    

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                script {
                    def now = new Date()
                    println now.getDay()
                    println "${params.DAY_ENV}"
                    params.DAY_ENV = now.getDay()
                    println now.format("yyMMdd.HHmm", TimeZone.getTimeZone('UTC'))
                }
            }
        }
    }
    post{
        always{
            emailext body: 'Test email body', subject: 'Test Email', to: 'abhijeetjain47@gmail.com'
        }
    }
}
