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
}
