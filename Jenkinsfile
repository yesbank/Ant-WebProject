//Declarative way
pipeline {
    agent any

    stages {
        stage('build') {
            steps {
		echo "My Branch Name: ${env.BRANCH_NAME}"
                sh 'ant'
            }
	}
    }
	
	post {
        success {
          emailext(
	    subject: "${env.JOB_NAME} ${env.BUILD_NUMBER} ${env.BUILD_STATUS} ",
            body: ${env.JOB_NAME} [${env.BUILD_NUMBER}]
            Check console output at '${env.BUILD_URL}'${env.JOB_NAME} ${env.BUILD_NUMBER},
            to: "devopstrainingblr@gmail.com"
          )
        }
      }
	
}
