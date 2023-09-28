pipeline {
  agent any
  stages{
      stage("build"){
          steps{
              echo 'Compiling sysfoo app...'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'Running unit tests...'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'Packaging sysfoo to war...'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
