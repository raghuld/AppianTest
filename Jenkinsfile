def scriptFileLocation
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
			echo 'Building..'
			scriptFileLocation='C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-versioning-client-2.5.12'
			bat 'dir'
			echo " My Script location ${scriptFileLocation}"
			bat "cd ${scriptFileLocation}"

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
