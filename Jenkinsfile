pipeline {
    agent any
    
    triggers {
        cron ('H/5 * * * *')
    
    stages {
        stage ('hello1') {
            when {
                triggeredBy 'TimerTrigger'
            }
            steps {
                echo 'hello, working'
            }
        }
        stage ('hello2') {
            steps {
                when {
                    not {
                        triggeredBy 'TimerTrigger'
                    }
                }
                echo 'hello, not working'
            }
        }
    }
}       
