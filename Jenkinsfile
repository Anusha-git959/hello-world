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
       }
     }
        stage('Run maven') {
      steps {
	sh 'mvn clean install package'
    deploy adapters: [tomcat9(credentialsId: 'jenkinstomcatdeployment', url: 'http://ec2-107-23-86-246.compute-1.amazonaws.com:8090/')], contextPath: 'Null', war: '**/*.war'    
      }
    }
  }
}

