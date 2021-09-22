pipeline {
agent any
  environment {
   PATH = "/usr/bin/mvn:$PATH"
  }
   stages { 
    stage("Clean code") { 
      steps { 
      sh "git clone https://github.com/girishgmn/impala"
      }
      }
      stage("build code"){
      steps{
         sh "mvn clean install"
      }
    }
    }
    }
                
