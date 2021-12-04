pipeline{
agent 'any'
tools{
maven 'M3'
// jdk 'JAVA_HOME'
}
stages {
stage('Checkout'){
steps{
git branch: 'master', url: 'https://github.com/SWATI-22/Buzztalk_jenkins.git'
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
bat 'java -jar C:/Program Files (x86)/Jenkin/workspace/test12/Buzztalk/target/Buzztalk-0.0.1-SNAPSHOT.jar'
}
}
}
}
