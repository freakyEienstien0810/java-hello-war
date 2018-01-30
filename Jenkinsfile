pipeline {
    agent {
       label "master" 
    }
    tool {
      maven "maven"
    }
    stages {
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                sh "'${mvnHome}/bin/mvn' deploy"
            }
        }
    }
}
