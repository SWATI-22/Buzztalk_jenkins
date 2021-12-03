


pipeline{
agent any


tools{maven 'M3'}

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
bat 'java -jar "C:/Program Files (x86)/Jenkins/workspace/buzztalk4/target/simple-maven-project-with-tests-1.0-SNAPSHOT.jar"'
}
}





}
}
