@Library("mylibrary")_
node('built-in')
{
    stage('ContDownload-Master')
    {
        cicd.newGit("maven")
    }
    stage('ContBuild-Master')
    {
        cicd.newMaven()
    }    
    stage('ContDeployment-Master')
    {
        cicd.newDeploy("ScriptedPipelinewithSharedlibraries","172.31.31.39","testapp")
    }
    stage('ContTesting-Master')
    {
        cicd.newGit("FunctionalTesting")
        cicd.executeSelenium("ScriptedPipelinewithSharedlibraries")
    }
    stage('ContDelivery-Master')
    {
        cicd.newDeploy("ScriptedPipelinewithSharedlibraries","172.31.20.75","prodapp")
    }
    
    
    
}
