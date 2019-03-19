pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'env'
                sh 'pwd'
                sh 'id -u'
                sh 'id -u -n'
                sh 'ls -al /root/.m2'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
