pipeline {

  /*
   * Run everything on an existing agent configured with a label 'jk-slave-agents'.
   */
  agent any

  stages {
    stage('Build and Publish Image') {
      steps {
        dir("/home/centos/workspace/week-1-lession-2-task/pipelinedemo/pipelinedemo") {
       sh 'mvn install clean'
         sh 'mvn package'
        }
      }
    }
  }
}














