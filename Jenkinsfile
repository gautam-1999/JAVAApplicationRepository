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
          sh '/opt/oracle/middleware/oracle_common/modules/org.apache.maven_3.2.5/bin/mvn pre-integration-test'
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