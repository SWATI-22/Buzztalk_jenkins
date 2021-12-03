// pipeline{
// agent any

// 		stages {
// 			stage('Verify Branch'){
// 			steps{
// 			echo "@GIT_BRANCH"
			
// 			}
// 			}
		
//             			stage('Hello'){
//             			steps{
//             			echo "Hello world....!!!"

//             			}

// 		                }
// 	                }
// }


pipeline{
agent any
tools{maven 'M3'}
stages{
stage('Checkout'){
steps{
git branch: 'main', url: 'https://github.com/SWATI-22/Buzztalk_jenkins.git'
}
}

stage('build')
{
steps {
bat 'mvn --version'
}

}
stage('Test'){
steps{
bat 'mvn test'
}
}
stage('Package'){
steps{
bat 'mvn package'
}
}
	stage('Deploy')
{
steps{
sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
}
}
}
