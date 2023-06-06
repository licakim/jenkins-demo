pipeline {
    agent {
        label "demoAgent"
    }
    stages {
        stage('git') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'main', credentialsId: 'lica-jenkins', url: 'https://github.com/licakim/jenkins-demo.git'

            }
        }
        stage('mvn') {
            steps {
                // Get some code from a GitHub repository
                    sh 'mvn -Dmaven.test.failure.ignore=true clean test'
            }
        }
    }
}
