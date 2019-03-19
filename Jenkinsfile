pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /disk2/jenkins/.m2:/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'env'
                sh 'pwd'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
