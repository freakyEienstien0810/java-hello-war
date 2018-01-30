pipeline {
    agent {
       label "master" 
    }
    tools {
      maven "mvn3.4"
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
                script {
                    withMaven(mavenSettingsConfig: '5deea8ee-d268-40da-b255-5f1dde2f4f0e'){
                    
                       sh "mvn deploy"
                    }
               }
            }
        }
    }
}
