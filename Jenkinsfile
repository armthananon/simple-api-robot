pipeline {
    agent any

    stages {
        stage('clone simple-api-robot') {
            agent { label 'test' }
            steps {
                sh 'git clone https://github.com/armthananon/simple-api-robot'
            }
        }
        stage('run robot test') {
            agent { label 'test' }
            steps {
                sh 'pip install robotframework-requests'
                sh 'cd simple-api-robot && robot test-calculate.robot'
            }
        }
    }
}
