pipeline {
    agent {
       label "master" 
    }
    tools {
      maven "mvn3.4"
    }
    stage('Build') {
        steps {
            bat "mvn clean package"
        }
    }
}
