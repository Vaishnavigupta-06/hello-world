pipeline {
    agent any
    tools {
        maven "MAVEN"
        jdk "JDK"
    }
    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
        stage('Build') {
            steps {
                
                sh 'mvn -B -DskipTests clean package'
                
            }
        }
     }
    post{
        success{
            mail to: "aayush.bisht@knoldus.com",
            subject: "Build is successfull",
  body: "success"    
        }     
    failure{
mail to: "vaishnavi.g@knoldus.com",
  subody: "failed"
 }
  }
  
}
