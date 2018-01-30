pipeline {
    agent {
       label "master" 
    }
    tools {
      maven "maven"
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn deploy"
            }
        }
    }
}
