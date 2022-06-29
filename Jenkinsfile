pipeline {
    agent {label "aws-virginia"}
    environment {
        PATH = "/opt/apache-maven-3.8.6/apache-maven/src/bin:$PATH"
    }
    stages {
        stage("Setting variables") {
            steps {
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage ('Test') {
            steps {
                sh 'maven test'
            }
        }
    }
}