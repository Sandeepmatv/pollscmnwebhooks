pipeline{
  
  agent any 
  
  options{
    buildDiscarder(logRotator(numToKeepStr: '2'))
    disableConcurrentBuilds()
    
  }
  
  triggers {
    pollSCM('* * * * *')
  }
  
  stages {
    stage('Declarative checkout') {
      steps {
        checkout scm
      }
    }
    stage('print file on screen'){
      steps{
        sh 'cat ci.txt'
      }
    }
  }
}
