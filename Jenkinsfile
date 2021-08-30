pipeline {
   // agent defines where the pipeline will run.
   agent {
       //Here we define that we wish to run on the agent with the label Node
   label "node1"
}
stages {
 stage('Declarative Checkout SCM')
{
 steps 
    {
	   echo 'Checkout SCM'
    }
}
 stage('creation of the folder')
     {
	steps
	{
		sh 'cd /home/ubuntu; sudo mkdir testfolder11'
	}
}
 stage('creating the folder on different server')
    {
	steps {
		label ('node2')
	
	    sh 'cd /home/ubuntu; sudo mkdir jenkins11'
		}
	}
}
}
