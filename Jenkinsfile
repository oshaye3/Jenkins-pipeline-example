pipeline {

  /*
   * Run everything on an existing agent configured with a label 'jk-slave-agents'.
   */
  agent any

  stages {
    stage('Build and Publish Image') {
      steps {
        
       sh 'sudo mvn install clean'
      }
    }
  }
}
