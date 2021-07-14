pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
				def scriptFileLocation="C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-versioning-client-2.5.12/version-manager.properties";
				echo "My variable is ${scriptFileLocation}";
				bat 'cd ${scriptFileLocation}';

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
