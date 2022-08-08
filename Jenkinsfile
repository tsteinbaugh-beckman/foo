pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'main' || env.BRANCH_NAME == 'master') {
                        echo "this is a main branch"
                    }
                    else if (env.BRANCH_NAME == 'feature') {
                        echo "this is a feature branch"
                    }
                    else {
                        echo "unknown branch name"
                    }
                }
            }
        }
    }
}
/*
        stage ('build next foo2') {
            steps {
                build job: 'test/foo2/main', propagate: false, wait: false
            }
        }
    }
}    

*/
