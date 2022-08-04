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
                script {
                    try {
                        build job: "test/foo2/${env.BRANCH_NAME}", propagate: false, wait: false
                    }
                    catch (err) {
                        build job: 'test/foo2/main', propagate: false, wait: false
                    }
                }
            }
        }
    }
}    
