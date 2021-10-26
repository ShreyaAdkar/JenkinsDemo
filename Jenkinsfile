
pipeline {
    agent any 
    stages{
        stage('Deploy'){
            //agent { label 'windows' }
            steps{
                //deleteDir()
                //sh 'mkdir -p archive'
                //sh 'echo Output > archive/Output.txt'
                script{
                    zip archive : true, dir : '', glob : '', zipFile : 'Output.zip'
                } 
            }
        }
    }
}
rtUpload (
   serverId: "artifactory",
    spec: '''{
          "files": [
            {
              "pattern": "C:/Windows/System32/config/systemprofile/AppData/Local/Jenkins/.jenkins/workspace/JenkinsDemo/Output.zip",
              "target": "demo2/"
              "recursive" : "false"
            }
         ]
    }'''
 
    // Optional - Associate the uploaded files with the following custom build name and build number,
    // as build artifacts.
    // If not set, the files will be associated with the default build name and build number (i.e the
    // the Jenkins job name and number).
    //buildName: 'holyFrog',
   //buildNumber: '42',
    // Optional - Only if this build is associated with a project in Artifactory, set the project key as follows.
   // project: 'my-project-key'
)
