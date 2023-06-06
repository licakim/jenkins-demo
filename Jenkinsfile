pipeline {
    environment {
    JAVA_HOME = '/usr/lib/jvm/java-11-openjdk-amd64'
}
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
                tools{
                    maven 'Maven 3.9.2'
                }
                    sh 'mvn -Dmaven.test.failure.ignore=true clean test'
            }
        }
    }
}
