pipeline {
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
                sh 'mvn test'
            }
        }
    }
}