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
        stage('Build'){

steps{

sh 'mvn compile'

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

stage('Deploy')

{

steps{

sh 'java -jar /var/lib/jenkins/workspace/buzztalk4/target/*.jar'

}
        }
    }
}
