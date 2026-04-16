pipeline{
	agent any
	
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
		stage('Checkout'){
			steps{
				git branch: 'main', url: 'https://github.com/stutimahesh/MyGradleApp.git'
			}
		}
		stage('Build'){
			steps{
				sh './gradlew build'
			}
		}
		stage('Test'){
			steps{
				sh './gradlew test'
			}
		}
		stage('Run Application'){
			steps{
				sh './gradlew run'
			}
		}
	}
	
	post{
		success{
			echo 'Build and deployment successful'
		}
		failure{
			echo 'Build failed!'
		}
	}

}
