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
sh 'mvn --version'
}

}
stage('Test'){
steps{
sh 'mvn test'
}
}
stage('Package'){
steps{
sh 'mvn package'
}
}
}
}
