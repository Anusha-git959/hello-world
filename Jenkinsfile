pipeline {
  agent any
      stages {
        stage ('one') {
           steps{ 
              echo 'hi, this is anusha'
           }
        }
       
        stage('scm') {
         steps { 
           // some block
           git url: 'https://github.com/Anusha-git959/hello-world.git'
        }
     }

        stage('build') {
           steps {
            sh 'mvn clean install package'
         }   
     } 
        stage ('deployment') {
          steps{
            sshagent(['Tomcat_pipeline']) {
              sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ubuntu@52.91.13.163:/opt/apache-tomcat-9.0.95/webapps'

            }
          }
        }
 } 

}

