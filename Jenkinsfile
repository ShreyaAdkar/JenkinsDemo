
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
        stage ('Upload') {
            steps {
                rtUpload (
                    //buildName: 'holyFrog',
                    //buildNumber: '42',
                    // Obtain an Artifactory server instance, defined in Jenkins --> Manage Jenkins --> Configure System:
                    serverId: "artifactory1234",
                   specPath: 'C:/Windows/System32/config/systemprofile/AppData/Local/Jenkins/.jenkins/workspace/JenkinsDemo/upload.json'
                    //specPath: 'https://github.com/ShreyaAdkar/JenkinsDemo/blob/main/upload.json'
                )
            }
        }
     }
 }
