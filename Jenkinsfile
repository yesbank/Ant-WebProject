#! groovy
node{
 stage('Source'){
     git 'https://github.com/devopstrainingblr/Ant-WebProject.git'
 }
 
 stage('Build'){
    // def mvnHome = tool 'maven3'
    sh "ant -f build-mt.xml" 
 }
 stage('Send Email'){
     mail bcc: '', body: 'Demo Pipeline', cc: '', from: '', replyTo: '', subject: 'Pipeline Demo', to: 'devopstrainingblr@gmail.com'
 }
 stage('Archive'){
  archiveArtifacts '/Users/bhaskarreddyl/.jenkins/workspace/Pipeline-Project-Ant-Web/dist/*.war'
 }
}
