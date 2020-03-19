properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', 
                                      artifactNumToKeepStr: '', 
                                      daysToKeepStr: '7', 
                                      numToKeepStr: '6')), 
            disableConcurrentBuilds(), 
            parameters([string(description: '', name: 'RESULT_URL'), 
                        string(description: '', name: 'RESULT_METRIC')])])
node {
  checkout scm
  stage ('First step') {
  }
  stage ('Second step') {
  }
  stage ('Third step') {
  }
  withEnv(['HTTP_PROXY=', 'HTTPS_PROXY=']) {
    def post = new URL("${RESULT_URL}").openConnection()
    def message = "${RESULT_METRIC} 1\n"
    post.setRequestMethod("POST")
    post.setDoOutput(true)
    post.getOutputStream().write(message.getBytes("UTF-8"));
    def postRC = post.getResponseCode();
    println(postRC);
  }
}
