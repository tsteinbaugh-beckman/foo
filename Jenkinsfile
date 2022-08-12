pipeline {
    agent any
    
    stages {
        stage ('hello') {
            steps {
                script {
                    var = "s3://beckman-build-artifacts/docs/com.beckman.particle.pathfinder/pathfinder-customerportal-backend/0.0.47/./"
                    assert "0.0.47" ==~ /(\d+\.\d+\.\d+)$/
                    while (var !=~ /.*(\d+\.\d+\.\d+)$/) {
                        var = var.substring(0, var.length() - 1)
                        println var
                    }
                    println var
                }
            }
        }
    }
}
