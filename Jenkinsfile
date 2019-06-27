pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
    post {
            always {
                echo 'Pipeline has completed'
            }
            success {
                echo 'The full pipeline was successful'
            }
            failure {
                echo 'There was a problem in the pipeline'
            }
            unstable {
                echo 'The pipeline run was unstable'
            }
            changed {
                echo 'The state of the pipeline has changed'
                echo 'For example, if the Pipeline was previously failing but is now successful'
            }
    }
}