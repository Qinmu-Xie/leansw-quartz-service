pipeline {
    agent {
      docker {
        image 'maven:3.3.3'
        args '-v /var/lib/jenkins/conf/settings.xml:/root/.m2/settings.xml'
      }
    }
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
