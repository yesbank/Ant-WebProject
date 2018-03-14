#! groovy
node{
 stage('Source'){
     git 'https://github.com/devopstrainingblr/Ant-WebProject.git'
 }
 
 stage('Build'){
    
    cmd "ant -f build-mt.xml" 
 }
 stage('Send Email'){
     mail bcc: 'mithunreddytechnologies@gmail.com', body: 'Buils is done', cc: '', from: '', replyTo: '', subject: 'Build Status', to: 'devopstrainingblr@gmail.com'
 }
 /*stage('Archive'){
  archiveArtifacts '/Users/bhaskarreddyl/.jenkins/workspace/Pipeline-Project-Ant-Web/dist/SampleAntProject.war'
 }*/
}
