pipeline {
    agent {label 'pathfinder'}
    options {
        buildDiscarder logRotator( 
                    daysToKeepStr: '7', 
                    numToKeepStr: '10'
            )
            }
  stages {
        stage ('feature branch testing: Maven') {
          when {
                branch pattern: "feature-\\d+", comparator: "REGEXP"
            }
            steps {
              echo 'test1'
                }
            }
        }
      stage ('Pull request for Main branch pull') {
         when {
                changeRequest target: "main"
            }
        steps {
          echo 'test2'
        }
      }
      stage('Verify branch syntax') {
            when {
                not {
                    branch "main"
                }
                not {
                    branch pattern: "feature-\\d+", comparator: "REGEXP"
                }
                not {
                    branch "PR-*"
                }
            }
            steps {
                error "invalid branch name - expected feature-#"
           }
        }
    }
}
