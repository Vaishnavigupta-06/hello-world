pipeline{
  agent{
  agent any
  }
  stages{
    stage("clone"){
      steps{
      git 'https://github.com/Vaishnavigupta-06/hello-world.git'
      
      
      }
    
    
    }
    stage("build"){
      steps{
     sh 'mvn clean package'
      
      }
    
    }
  
  }





}
