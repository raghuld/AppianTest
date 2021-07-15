
pipeline {
    agent any

	parameters {
        string(name: 'vcUsername', description: 'Git User Name')
        string(name: 'vcPassword', description: 'Git Password')
        string(name: 'repoUrl', description: 'Git URL')
        string(name: 'uuid', description: 'Application UUID to generate package')
		string(name: 'applicationPath', description: 'Path to generate package and import')
		string(name: 'appianURL', description: 'Appian URL ending with suite')
		string(name: 'appianUsername', description: 'Appian Username')
		string(name: 'appianPassword', description: 'Appian Password')
    }
    stages {
        stage('Build') {
            steps {
			script{
			echo 'Building Zip files from Git..'
			bat 'dir'
				dir('C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-versioning-client-2.5.12') {
    // some block
    	    bat "version-application -vc_username ${params.vcUsername} -vc_password ${params.vcPassword} -repo_url ${params.repoUrl} -action buildSingleApp -uuid ${uuid} -package_path \"${applicationPath}\" "
				}
		
			echo 'Importing Zip files to appian..'
			dir('C:/Users/raghuld/POC Github Jenkins/Deployment Automation Manager/appian-adm-import-client-2.5.12') {
			// Execute Script
				echo "deploy-application -application_path \"${applicationPath}\""
				bat "deploy-application -application_path \"${applicationPath}\" -url ${appianURL} -username ${appianUsername} -password ${appianPassword}"
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
