pipeline
{
  agent any
  stages
  {
    
    stage ('git clone')
    { steps
          {  sh 'echo downloading code' }
     }
    
    stage ('code build')
    { steps
     {   sh 'echo code is building'    }
    }
     
    stage ('get apprvoal')
    { steps 
    { input "please approve the deployment?" }
    }
    
    
    
    stage ('deployments')
    { steps
     { sh 'echo code is deploying' }
    }
  }
}
