pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    var = "123456789"
                    while (var !=~ "/(7)$/") {
                        var = var.substring(0, var.length() - 1)
                        println var
                    }
                    println var
                }
            }
        }
    }
}
