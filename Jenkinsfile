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
  def post = new URL($RESULT_URL).openConnection()
  def message = $RESULT_METRIC + ' 1'
  post.setRequestMethod("POST")
  post.setDoOutput(true)
  post.getOutputStrem().write(message.getBytes("UTF-8"));
  def postRC = post.getResponseCode;
  println(postRC);
}
