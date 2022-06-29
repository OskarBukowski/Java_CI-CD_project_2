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

            stage ('Build') {
                steps {
                    sh 'mvn -Dmaven.test.failure.ignore=true install'
                }
                post {
                    success {
                        junit 'target/surefire-reports/**/*.xml'
                    }
                }
            }

            stage ('Build') {
                steps {
                    sh 'mvn test'
                }
            }
        }
}