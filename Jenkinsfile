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
                echo "M3_HOME = ${M3_HOME}"
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