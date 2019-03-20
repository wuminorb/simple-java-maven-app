pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /disk2/jenkins/.m2:/var/maven/.m2 -u 1000 -e MAVEN_CONFIG=/var/maven/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'env'
                sh 'pwd'
                sh 'id -u'
                sh 'mvn -Duser.home=/var/maven -DskipTests clean package'
            }
        }
    }
}
