pipeline {
    agent any

    

    stages {
        stage('Initialize'){
            steps{
                echo "PATH = $PATH:$HOME/bin:$JAVA_HOME:$MAVEN_HOME:$M2"
                echo "M2 = /opt/apache-maven-3.8.1/bin"
            }
        }
        stage('Build') {
            steps {
                dir("/var/lib/jenkins/workspace/pipelinedemo/my-app") {
                sh 'mvn -B -DskipTests clean package'
                }
            
            }
        }
     }
    post {
       always {
          junit(
        allowEmptyResults: true,
        testResults: '*/test-reports/.xml'
      )
      }
   } 
}
