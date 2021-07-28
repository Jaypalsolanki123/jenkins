pipeline{
  agent any
  environment{
    PATH = "/usr/share/maven/bin:$PATH"
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
        sh  "sudo cp -r /home/jaypalsinh/Downloads/ /var/lib/tomcat9/webapps/"
      }
    }
    stage("WarFileDeploy"){
      steps{
        sh systemctl restart tomcat9
      }
    }
  }
}
