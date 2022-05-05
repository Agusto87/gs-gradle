node {
  def myGradleContainer = docker.image('gradle:7.4.2-jdk8')
  myGradleContainer.pull()
  stage('SCM check y Preparacion') {
    checkout scm
  }
  stage('Testeo') {
     myGradleContainer.inside("-v ${env.HOME}/.gradle:/home/gradle/.gradle") {
       sh 'cd complete && gradle test'
     }
  }
  stage('Ejecucion') {
     myGradleContainer.inside("-v ${env.HOME}/.gradle:/home/gradle/.gradle") {
       sh 'cd complete && gradle run'
     }
  }
}
