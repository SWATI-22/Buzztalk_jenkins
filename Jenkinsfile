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
tools{
maven 'apache-maven-3.8.3'
}

stages {
stage('Verify Branch'){
steps{
echo "@GIT_BRANCH"



}
}
stage('Checkout'){
steps{
git branch: 'main', url: 'https://github.com/SWATI-22/Buzztalk_jenkins.git'
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

stage('Test'){
steps{
bat 'mvn test'
}
}
stage('Deploy'){
steps{
bat 'java -jar "C:/Program Files (x86)/Jenkins/workspace/Buzztalk2/Buzztalk/.mvn/wrapper/maven-wrapper.jar"'
}
}





}
}
