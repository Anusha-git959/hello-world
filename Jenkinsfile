pipeline {
      agent any
            stages {
                    stage('One') {
                           steps {
                                   echo 'hi, thi is kumar'
                                   }
                                   }
                   stage('two') {
                            steps {
                                   input('Do tou want to proceed?')
                                   }
                                   }
                    stage('scm') {
                            steps {
                                  //some block
                                  git 'https://github.com/kumarnakka/hello-world.git'
                                   }
                                   }
                   stage('packaging') {
                          steps {
                          sh label: '', script: 'mvn package'
                          }
                          }
}
}
