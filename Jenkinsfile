pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
			script{
			echo 'Building..'
			def scriptFileLocation='C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-versioning-client-2.5.12'
			bat 'dir'
			echo " My Script location ${scriptFileLocation}"
			bat "copy ${scriptFileLocation}"
			bat 'dir'
			bat 'version-application.bat'
			}
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
