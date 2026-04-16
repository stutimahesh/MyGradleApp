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
				dir('app') {
            sh '../gradlew build'
        }
			}
		}
		stage('Test'){
			steps{
				dir('app') {
            sh '../gradlew build'
        }
			}
		}
		stage('Run Application'){
			steps{
				dir('app') {
            sh '../gradlew build'
        }
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
