pipeline {
    agent any
    
    triggers {
        cron(env.BRANCH_NAME == 'main' || env.RANC_NAME == 'master' ? 'H/5 * * * *' : '')
    }
    
    stages {
        stage ('hello') {
            steps {
                echo 'hello'
            }
        }
    }
}       
