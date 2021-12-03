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
agent{label 'master'}
tools{maven 'M3'}
stages{
stage('Checkout'){
steps{
git branch: 'master', url: 'https://github.com/SWATI-22/Buzztalk_jenkins.git'
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
}
}
