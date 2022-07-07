pipeline {
    agent any
    
    triggers {
        cron(env.BRANCH_NAME == 'main' ? 'H/5 * * * *' : '')
    }
    
    stages {
        stage ('hello') {
            steps {
                echo 'hello'
            }
        }
    }
}       
