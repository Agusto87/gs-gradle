node {
  def myGradleContainer = docker.image('gradle:7.4.2-jdk8')
  myGradleContainer.pull()
  stage('SCM check y Preparacion') {
    checkout scm
  }
}
