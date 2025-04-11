pipeline{
 // need to add agents
 agent any
 
 tools{
 // here mymaven is tool configured under global tool configuration
 // new tools added
 maven 'maven'
 }
 
 stages{
 
 stage('Clone repo')
 
 {
 steps{
 git 'https://github.com/neha0814/Jenkinsfile_project.git'
 }
 }
 
 stage('Compile Code')
 {
 steps{
 
 sh 'mvn compile'
 }
 }
 
 stage('Test Code')
 {
 
 steps{
 
 sh 'mvn test'
 }
 post{
 success{
 junit 'target/surefire-reports/*.xml'
 }
 }
 }
 stage('Package Code')
 {
 steps{
 
 sh 'mvn package'
 }
 }
 }
}
