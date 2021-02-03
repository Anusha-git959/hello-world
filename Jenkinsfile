pipeline {
  agent any {
      stages{
       stage('scm checkout'){
       git ('https://github.com/kumarnakka/hello-world.git')
       }
       stage('compile stage'){
         steps{
         with maven(maven: 'maven-3'){
         sh 'mvn clean compile'
        }
       }
     }
         stage('test stage'){
           steps{
           with maven(maven: 'maven-3'){
           sh 'mvn test'
           }
           }
         }
         stage('package stage')
          steps{
            with maven(maven: 'maven-3'){
             sh 'mvn package'
              
           }
         }
   }

