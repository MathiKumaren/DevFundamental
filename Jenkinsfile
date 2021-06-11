#!groovy

node('node') {
    currentBuild.result = "SUCCESS"

    try
	{
       stage('Checkout')
	   {
          checkout scm
       }
	   stage('Deploy')
	   {
         echo 'Push to Repo'
       }
	   stage('Archive')
		archive 'ProjectName/bin/Release/**'
	}
	catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }
}
