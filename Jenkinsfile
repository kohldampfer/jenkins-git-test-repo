node('master') {
	checkout scm
	stage('build') {
		withMaven {
			sh 'mvn clean install'
		}
	}
}
