pipeline {
    agent any
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
                sh 'mvn test'
            }
        }
    }
}