
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
				def fileName="'C:\\\\Windows\\\\system32\\\\config\\\\systemprofile\\\\AppData\\\\Local\\Jenkins\\\\.jenkins\\\\workspace\\\\Pipeline script from SCM\\\\${zipFileName}'"
				echo "deploy-application -application_path ${fileName}"
				bat "deploy-application -application_path ${fileName}"
			}
			}
            }
        }
      
    }
	post { 
        always { 
            cleanWs()
        }
    }
}
