pipeline {
	agent any
	stages {
		stage('Upload to AWS'){
			steps{
				withAWS(region:'us-east-1',credentials:'aws-project3'){
					s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'udacity-jenkins-project3')
				}
			}
		}
	}
}