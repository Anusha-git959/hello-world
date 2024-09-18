pipeline {
  agent any
      stages {
        stage ('folder') {
           steps{ 
             sh 'mkdir demotest'
           }
        }
        stage('scm checkout'){
          steps { 
           input ('Do you want to proceed')
       }
     }
        stage('build'){
         steps {
         sh 'mvn clean install package'
        }
     }
         stage('copying') {
           steps {
            sh 'cp -r /var/lib/jenkins/workspace/demo-freestyle-job/webapp/*  demotest'
         }   
     }      

 } 
}


