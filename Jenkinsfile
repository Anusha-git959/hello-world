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
  }
}

