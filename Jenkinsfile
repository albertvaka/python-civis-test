pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'DD_SERVICE=my-python-app DD_ENV=ci pytest --ddtrace'
            }
        }
    }
}

