pipeline {
    agent any

    stages {

        stage('Deploy') {
            steps {
                echo 'Downstream deployment started...'
                echo 'Application deployed successfully!'
            }
        }
    }

    post {
        success {
            echo 'Downstream Job Successful!'
        }

        failure {
            echo 'Downstream Job Failed!'
        }
    }
}
