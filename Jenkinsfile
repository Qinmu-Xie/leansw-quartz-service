pipeline {
    agent { docker 'maven:3.3.3' }
    stages {
        stage('cobertura') {
            steps {
                sh 'mvn clean cobertura:cobertura'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
