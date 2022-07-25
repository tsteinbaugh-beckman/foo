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
                if ("test/foo2/${env.BRANCH_NAME}" == true),{
                    build job: "test/foo2/${env.BRANCH_NAME}", propagate: false, wait: false
                }
                else {
                    build job: 'test/foo2/main', propagate: false, wait: false
                }
            }
        }
    }
}    
