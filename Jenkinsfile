pipeline {
  agent any
      stages {
       stage('scm checkout'){
         steps {
         git url: 'https://github.com/kumarnakka/hello-world.git'
       }
     }
       stage('build'){
         steps {
         sh 'mvn clean install package'
         deploy adapters: [Tomcat:9.x(credentialsId: 'tomcat_jenkins', url: 'http://ec2-54-242-80-19.compute-1.amazonaws.com:8090/')], contextPath: 'Null', war: '**/*.war' 
       }
     }   
  }
}

