pipeline {

  /*
   * Run everything on an existing agent configured with a label 'jk-slave-agents'.
   */
  agent any

  stages {
    stage('Build and Publish Image') {
      steps {
        dir("/var/lib/jenkins/workspace/pipelinedemo/my-app") {
       sh 'mvn install clean'
         sh 'mvn package'
        }
      }
    }
  }
}
