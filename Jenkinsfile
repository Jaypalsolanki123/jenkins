pipeline{
  agent any
  environment{
    PATH = "/usr/bin:$PATH"
  }
  stages{
    stage("GitCheckOut"){
      steps{
        echo "This is my first Declarative Pipeline"
      }
    }
    stage("MavenBuild"){
      steps{
        sh "mvn clean package"
      }
    }
  }
}
