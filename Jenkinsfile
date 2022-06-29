pipeline {
    agent {label "aws-virginia"}
    stages {
        stage("Setting variables") {
            steps {
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
        stage ('Testing') {
            steps {
                sh 'pwd'
            }
        }
    }
}