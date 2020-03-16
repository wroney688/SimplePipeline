properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', 
                                      artifactNumToKeepStr: '', 
                                      daysToKeepStr: '7', 
                                      numToKeepStr: '6')), 
            disableConcurrentBuilds()]), 
            parameters([string(description: '', name: 'RESULT_URL'), 
                        string(description: '', name: 'RESULT_METRIC')])
node {
  checkout scm
  stage ('First step') {
  }
  stage ('Second step') {
  }
  stage ('Third step') {
  }
}
