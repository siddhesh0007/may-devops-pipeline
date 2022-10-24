pipeline
{
  agent any
  stages
  {
    stage ('scm checkout')
    {
      steps
      { git branch: 'master', url: 'https://github.com/prakashk0301/maven-project' }
    }
    stage ('please compile code')
    {
      steps
      { withMavenjdk: 'localjdk-1.8', maven: 'localmaven')
       { sh 'mvn compile'
       }
      }
    }
    
    stage ('please test code')
    {
      steps
      { withMavenjdk: 'localjdk-1.8', maven: 'localmaven')
       { sh 'mvn compile'
       }
      }
    }
    
    
  }
}
