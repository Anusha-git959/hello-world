pipeline {
  agent any
      stages {
        stage ('one') {
           steps{ 
             sh 'echo 'hi', this is anusha'
           }
        }
        stage('scm checkout'){
          steps { 
           input ('Do you want to proceed')
        
       }
     }
        stage('scm'){
         steps { 
           // some block
           git url: 'https://github.com/Anusha-git959/hello-world.git'
        }
     }

        stage('packaging') {
           steps {
            sh label: '', script:'mvn package'
         }   
     }      
 } 
}

