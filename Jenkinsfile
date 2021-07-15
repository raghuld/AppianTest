pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
			script{
			echo 'Building..'
			bat 'dir'
			zip dir: 'application_files', exclude: '', glob: '', zipFile: 'TimerComponent_Sample application'			}
            }
        }
      
    }
}
