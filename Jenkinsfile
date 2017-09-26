pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        echo '"Running ${env.BUILD_ID} on ${env.JENKINS_URL}"'
      }
    }
    stage('Build') {
      steps {
        echo 'Building..'
        sleep 5
        isUnix()
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        sh './helloworld.sh'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
        sleep 5
        echo 'Done.'
      }
    }
  }
}