pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    echo "${CHANGE_ID}"
                }
            }
        }
    }
}
