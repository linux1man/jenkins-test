pipeline {
    agent any
    stages {
        stage('UnitTest') {
            steps {
                sh 'echo "Testing Complete"'
            }
        }
        stage('Integration Test') {
            steps {
                sh 'echo "Integration Test Complete"'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
                sh 'echo "Hello Pipeline"'
                sh 'ls -al'
                sh 'pwd'
            }
        }
        stage('Deploy App') {
            steps {
                sh 'echo "App Deployed"'
            }
        }
    }
}
