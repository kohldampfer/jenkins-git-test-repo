node('master') {
	stage('scm') {
		checkout([
			$class: 'GitSCM',
			branches: [[name: '*/master']],
			doGenerateSubmoduleConfigurations: false,
			extensions: [],
			submoduleCfg: [],
			userRemoteConfigs: [[url: 'https://github.com/kohldampfer/jenkins-git-test-repo']]
			])
	}

	stage('build') {
		withMaven(jdk: 'Default Java', maven: 'Default Maven') {
			sh 'mvn clean install'
		}
	}
}
