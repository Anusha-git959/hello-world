pipeline {
  agent any
      stages {
       stage('scm checkout'){
       git ('https://github.com/kumarnakka/hello-world.git')
       }
       stage('compile stage'){
         steps {
         sh 'mvn clean compile'
       }
     }
         stage('test stage'){
           steps {
           sh 'mvn test'
           }
         }
         stage('package stage'){
          steps {
             sh 'mvn package'
              
           }
         
   }
  }
}

