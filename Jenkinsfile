pipeline{
	agent any
	tools{
		maven 'M3'
		jdk 'JAVA_HOME'
	}
	stages {
		stage('Checkout'){
			steps{
				git branch: 'main', url: 'https://github.com/Gsardhana/Buzzztalk.git'
			}
		}
		stage('Build'){
			steps{
				bat 'mvn compile'
			}
		}
		stage('Package'){
			steps{
				bat 'mvn package'
			}
		}
		stage('Deploy'){
			steps{
				bat 'java -jar C:/Program Files (x86)/Jenkins/workspace/Buzztalk/target/Buzztalk-0.0.1-SNAPSHOT.jar'
			}
		}
	}
}
