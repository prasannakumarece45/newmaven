@Library("mylibrary")_
node('built-in')
{
    stage('ContDownload-Loans')
    {
        cicd.newGit("maven")
    }
    stage('ContBuild-Loans')
    {
        cicd.newMaven()
    }    
    
    
    
}
