pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
				def scriptFileLocation='Hello'
				echo "My variable is ${scriptFileLocation}"

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
