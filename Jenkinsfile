pipeline{

  agent any
  
  stages {
    stage("build"){
      
      steps{
        echo 'building the application...'    
      }
      
    }
    
    stage("test"){
      
      steps {
        echo 'testing the application...'
        snykSecurity(
          severity: 'high',
          snykInstallation: 'snyk@latest',
          snykTokenId: 'organization-snyk-api-token',
          // place other parameters here
        )
      }
      
    }
    
    stage("deploy"){
      
      steps {
        echo 'deploying the application...'  
      } 
    } 
  }
}
