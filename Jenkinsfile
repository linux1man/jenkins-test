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
        sh '''echo "Preforming Integration Test"
echo "******25%"
echo "************50%"
echo "******************75%"
echo "************************100%"
echo "Integration Test Complete"
'''
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
        mail(subject: 'Success', body: 'Hi success ', from: 'x@x.com', to: 'y@y.com')
      }
    }

  }
}