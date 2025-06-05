pipeline{
 agent any
 tools{
   gradle 'Gradle'
   jdk 'JDK'
   }
  stages{
   stage('Checkout'){
    steps{
     git branch:'master',url: 'https://github.com/hanimalnad/gj.git'
     }
    }
    stage('Build'){
     steps{
      sh 'gradle build'
     }
    }
    stage('Test'){
     steps{
      sh 'gradle test'
     }
    }
    stage('Run Application'){
     steps{
      sh 'gradle run'
     }
    }
   }
   post{
    success{
     echo 'Build and Deployment successful!'
     }
    failure{
     echo 'Build failed.'
     }
    }
   }
      
    
