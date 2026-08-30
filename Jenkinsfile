pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Archive Artifact') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar',
                           fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'Upstream Maven Build Successful!'
        }

        failure {
            echo 'Upstream Maven Build Failed!'
        }
    }
}
