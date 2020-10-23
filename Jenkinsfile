pipeline {
  agent {
      label "maven"
  }
  stages {
    stage('Run maven') {
      steps {
	sh 'mvn -B -DskipTests clean package'
    deploy adapters: [tomcat9(credentialsId: 'sample-1', url: 'http://10.85.51.31:8080/')], contextPath: 'Null', war: '**/*.war'      }
	    pulishCppcheck allowNoReport: true, ignoreBlankFiles: true, pattern:
		    '**/Firmware/cppcheck.xml'
    }
  }
}
