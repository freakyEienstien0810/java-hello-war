pipeline {
    agent {
       labels "master" 
    }
    tool {
      maven = maven
    }
    stages {
        stage('preparation') {
            steps {
               mvnHome = tool 'maven' 
            }
        }
        stage('Build') {
            steps {
                sh "echo ${mvnHome}"
                sh "'${mvnHome}/bin/mvn' clean package"
            }
        }
        stage('Deploy') {
            steps {
                sh "'${mvnHome}/bin/mvn' deploy"
            }
        }
    }
}
