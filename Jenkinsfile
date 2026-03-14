node {
    stage('CheckOutCode')
    {
        git credentialsId: '17cbc593-ebf6-481d-8538-ceeee47a499e', url: 'https://github.com/M-sDevOpsCareer/Nodejs_project.git'
    }
    stage('build')
    {
        nodejs(nodeJSInstallationName: 'nodejs17.3.1')
        {
        sh "npm install"
        }
    }
    stage('ExecuteSonarQubeReport')
    {
       nodejs(nodeJSInstallationName: 'nodejs17.3.1')
       {
          sh "npm run sonar"
       }
    }

/*
stage('UploadArtifactsIntoNexus'){
sh "npm publish"
}
*/

stage('RunNodeJsApp'){
sh "npm start"
}

}

