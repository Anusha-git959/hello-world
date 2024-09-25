pipeline {
  agent any
      stages {
        stage ('one') {
           steps{ 
              echo 'hi, this is anusha'
           }
        }
       
        stage('scm'){
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
        stage ('deployment'){
          steps{
            sshagent([TOMCAT_ID]) {
              sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ubuntu@54.147.233.240:/opt/apache-tomcat-9.0.95/webapps'

            }
          }
        }
 } 

}

