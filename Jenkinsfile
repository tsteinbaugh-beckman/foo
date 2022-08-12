pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    var = "123456789999.0.0"
                    while !(var ==~ /(\d+\.\d+\.\d+)$/) {
                        var = var.substring(0, var.length() - 1)
                        println var
                    }
                    println var
                }
            }
        }
    }
}
