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
	   subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Successfull",
           body: "${env.JOB_NAME} [${env.BUILD_NUMBER}] ${env.BUILD_URL}"
           
            to: "devopstrainingblr@gmail.com"
          )
        }
		failure{
			emailext(
	   subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Failed...",
           body: """<p>'${env.JOB_NAME} [${env.BUILD_NUMBER}]'":</p>
            <p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>""",
            to: "devopstrainingblr@gmail.com"
          )
		}
      }
	
}
