pipeline
{
   agent any
   stages
   { 
       stage('scm checkout')
       {
           steps {
               git branch: 'master', url: 'https://github.com/prakashk0301/maven-project'
                 }
       }

       stage('please compile code')
       { steps {
           withMaven(jdk: 'localjdk', maven: 'localmaven') {
            sh 'mvn compile'
}
       }

       }
      
           stage('please test code')
       { steps {
           withMaven(jdk: 'localjdk', maven: 'localmaven') {
            sh 'mvn test'
}
       }

       }
        stage('please build code')
       { steps {
           withMaven(jdk: 'localjdk', maven: 'localmaven') {
            sh 'mvn package'
}
       }

       }
      
      stage('deploy to tomcat')
       {
         steps
          {

       sshagent(['944599ec-f52b-4aea-ad14-fe7d2900d14e']) {
       sh 'scp -o StrictHostKeyChecking=no */target/webapp.war ec2-user@172.31.20.192:/var/lib/tomcat/webapps'

}
}
}
  
   } 
}
