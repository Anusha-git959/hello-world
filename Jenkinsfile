pipeline {
  agent any
      stages {
        stage ('folder') {
           steps{ 
             sh 'mkdir demotest1'
           }
        }
        stage('scm checkout'){
          steps { 
           input ('Do you want to proceed')
           git url: 'https://github.com/Anusha-git959/hello-world.git'
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


