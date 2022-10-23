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
    
    stage ('deployment')
    { steps
     { sh 'echo code is deploying' }
    }
  }
}
