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
        pwd()
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
        fileExists 'helloworld.sh'
        sh 'echo "what goes in a shell script"'
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