pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "./helloworld.sh"
                if [ $? -ne 0 ] then
                  echo "Testing failed :("
                else
                  echo "Testing passed"
               fi
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sleep 5
                echo 'Done."
            }
        }
    }
}
