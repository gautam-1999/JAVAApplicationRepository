pipeline {
  agent {
    node {
      label 'soa12clab'
    }
    
  }
  stages {
    stage('PreBuild Action') {
      steps {
        echo 'Initiating the Build Process'
      }
    }
    stage('BuildAndDeploy') {
      steps {
        dir(path: 'JAVAApplicationDeploy') {
          git 'https://github.com/Indrayan123/CommonRepo'
        }
        
      }
    }
  }
  environment {
    adminurl = 't3://uxlab017:7001'
    weblogicuname = 'weblogic'
    weblogicpwd = 'weblogic1'
  }
}