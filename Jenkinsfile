@Library('mylibrary')_
node("built-in")
{
    stage('ContDownload_Master')
    {
        cicd.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    stage('ContBuild_Master')
    {
        cicd.newMaven()
    }
    stage('ContDeployment_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.5.241","testapp")
    }
    stage('ContTesting_Master')
    {
        cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
        cicd.runSelenium("ScriptedPipelinewithsharedlibraries")
    }
    stage('ContDelivery_Master')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.11.218","prodapp")
    }
}

