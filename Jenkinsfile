pipeline {
    agent none
    
    stages {
        stage ('hello') {
            steps {
                script {
                    var = "adsfasdfa123456789999.0.0564644654"
                    while (var !=~ /(.*)(\d+\.\d+\.\d+)$/) {
                        println "before: " + var
                        var = var.substring(0, var.length() - 1)
                        println "after: " + var 
                    }
                    println "end result: " + var
                }
            }
        }
    }
}
