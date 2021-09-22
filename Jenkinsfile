pipeline {
  environment {
    JAVA_TOOL_OPTIONS = "-duser.home=/var/maven"
  }
  agent {
  docker { 
    image "maven:3.8.2-adoptopenjdk-11"
    args "-v /root/.m2:/root/.m2"
  }
  }
  tools { 
  stages { 
    stage("build") { 
      steps { 
        sh "mvn --version"
        sh "mvn clean install"
      }
    }
  }
  post { 
    always { 
      cleanWs()
    }
  }
}
}
                
