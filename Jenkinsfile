// Powered by Infostretch 

timestamps {

node () {

	stage ('barclays-app - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GITHUB-CREDENTIALS', url: 'https://github.com/benadaba/maven-web-application']]]) 
	}
	stage ('barclays-app - Build') {
 			// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn validate " 
			} else { 
 				bat "mvn validate " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn test " 
			} else { 
 				bat "mvn test " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn sonar:sonar " 
			} else { 
 				bat "mvn sonar:sonar " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn deploy " 
			} else { 
 				bat "mvn deploy " 
			} 
 		} 
	}
	stage ('barclay-app-dev - Build') {
 			// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn validate " 
			} else { 
 				bat "mvn validate " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn test " 
			} else { 
 				bat "mvn test " 
			} 
 		}		// Maven build step
		withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn sonar:sonar " 
			} else { 
 				bat "mvn sonar:sonar " 
			} 
 		}
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn sonar:sonar " 
			} else { 
 				bat "mvn sonar:sonar " 
			} 
 		}		// Maven build step
	withMaven(maven: 'maven386') { 
 			if(isUnix()) {
 				sh "mvn deploy " 
			} else { 
 				bat "mvn deploy " 
			} 
 		} 
	}
}
}
