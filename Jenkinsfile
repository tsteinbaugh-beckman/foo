pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                echo 'hello'
            }
        }
        stage ('build next foo2') {
            steps {
                build job: 'test/foo2'
            }
        }
    }
}       
