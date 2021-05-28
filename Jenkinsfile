pipeline {
     agent any
     stages {
        stage("Install Dependencies") {
            steps {
                sh "npm install"
            }
        }
        stage("Build") {
            steps {
                sh "npm run build"
            }
        }
        stage("Test") {
            steps {
                sh "npm run test"
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'reports/**/*.html', fingerprint: true
            archiveArtifacts artifacts: 'dist/**', fingerprint: true
        }
    }

}
