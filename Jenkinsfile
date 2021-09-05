pipeline
{
agent any
stages
{  
    stage('scm checkout')                //stage name
    { steps                              //it tells jenkins to perform the activity 
     { sh 'echo code_is_downloading' }   //sh: execute command shell
    }


    stage('build the code')             //stage name, jenkins prints the stage
    { steps                             //tell jenkins to build the code
       { sh 'echo code_is_building'
         sh ' echo code_is_passed ' }   //execute steps in sequence you can provide multiple commands
    }
	
	stage('deploy to dev env')
	{
	 steps { sh 'echo deploying_artifacts_to_dev_env' }
	
	}
	
	
	
	stage('Approve QA deployment')
	
	{ steps  { input 'Please approve QA deployment' } }   //wait for approval
	
	
	
	
	stage('deploy to QA  env')                            //once approved then execute the stage
	{
	 steps { sh 'echo deploying_artifacts_to_QA_env' }
	
	}	
	
}

}
