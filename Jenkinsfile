#!groovy

node('master') {
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
	 echo 'This is MULBr pieline'	   
       }
	catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }
}
