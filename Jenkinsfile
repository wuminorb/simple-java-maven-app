pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /disk2/jenkins/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo $HOME'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
