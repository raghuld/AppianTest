
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
			script{
			echo 'Building..'
			bat 'dir'
			def zipFileName='TimerComponent_Sample application.zip'
			zip dir: 'application_files', exclude: '', glob: '', zipFile: 'TimerComponent_Sample application.zip'
			dir('C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-import-client-2.5.12') {
			// Execute Script
				echo "deploy-application -application_path ${WORKSPACE}/${zipFileName}"
				bat "deploy-application -application_path ${WORKSPACE}\\${zipFileName}"
			}
			}
            }
        }
      
    }
}
