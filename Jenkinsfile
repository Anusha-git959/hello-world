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
         git url: 'https://github.com/Anusha-git959/hello-world.git'
       }
     }
        stage('build'){
         steps {
         sh 'mvn clean install package'
        }
     }

 } 
}


