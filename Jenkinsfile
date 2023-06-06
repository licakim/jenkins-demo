pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'

            }
        }
        stage('mvn') {
            steps {
                // Get some code from a GitHub repository
                bat "mvn -Dmaven.test.failure.ignore=true clean test"

            }
        }
    }
}
