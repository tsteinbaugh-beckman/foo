pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    var = "123456789999"
                    while (!var =~ /(8)$/) {
                        var = var.substring(0, var.length() - 1)
                        println var
                    }
                    println var
                }
            }
        }
    }
}
