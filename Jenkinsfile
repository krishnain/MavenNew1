@Library('mylibrary')_
node("built-in")
{
    stage('ContDownload_Loans')
    {
        cicd.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    stage('ContBuild_Loans')
    {
        cicd.newMaven()
    }
}

