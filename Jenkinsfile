node 
{
    stage('CheckOutCode')
    {
        git credentialsId: '17cbc593-ebf6-481d-8538-ceeee47a499e', url: 'https://github.com/M-sDevOpsCareer/Nodejs_project.git'
    }
    stage('build')
        {
        sh "npm install"
        }
    stage('ExecuteSonarQubeReport')
         {
          sh "npm run sonar"
         }
}
