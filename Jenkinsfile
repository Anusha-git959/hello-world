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
         git url: 'https://github.com/kumarnakka/hello-world.git'
       }
     }
        stage('build'){
         steps {
         sh 'mvn clean install package'
        }
     }

        stage('copying') {
          steps {
            cp -r /var/lib/jenkins/workspace/demo-freestyle-job/webapp/target/*  demotest
         }   
      }     
 } 
}

