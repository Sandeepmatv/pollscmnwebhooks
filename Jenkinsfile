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
    stage('stage 1') {
      steps {
        sh 'echo stage1'
      }
    }
    stage('stage 2') {
      steps {
        sh 'echo stage2'
      }
    }
    stage('print file on screen'){
      steps{
        sh 'cat ci.txt'
      }
    }
  }
}
