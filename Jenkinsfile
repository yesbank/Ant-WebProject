#! groovy
node{
 stage('Source'){
     git 'https://github.com/yesbank/Ant-WebProject.git'
 }
 
 stage('Build'){
    
    CMD "ant -f build-mt.xml" 
 }
 stage('Send Email'){
     mail bcc: 'reddyyaswanth1@gmail.com', body: 'Buils is done', cc: '', from: '', replyTo: '', subject: 'Build Status', to: 'reddyyaswanth1@gmail.com'
 }
 /*stage('Archive'){
  archiveArtifacts '/Users/bhaskarreddyl/.jenkins/workspace/Pipeline-Project-Ant-Web/dist/SampleAntProject.war'
 }*/
}
