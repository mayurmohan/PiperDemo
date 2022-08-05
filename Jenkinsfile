@Library('piper-lib-os') _

node() {
  stage('init') {
    deleteDir()
    checkout scm
  }
  stage('deployIntegrationArtifact and Get MPL Status') {
  	   setupCommonPipelineEnvironment script: this
       integrationArtifactDeploy script: this
	   integrationArtifactGetMplStatus script: this
	   print "status:" 
	   print  commonPipelineEnvironment.getValue("integrationFlowMplStatus")
  }
}
