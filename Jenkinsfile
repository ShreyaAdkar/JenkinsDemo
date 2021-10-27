
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
                    zip archive : true, dir : '', glob : '', zipFile : 'Output2.zip'
                } 
            }
        }
        stage ('Upload') {
            steps {
                rtUpload (
                
                   serverId: "artifactory1234",
                    spec: '''{
                        "files": [
                            {
                             "pattern": "*.zip",
                             "target": "demo2/"
                            }
                        ]
                    }'''
                )//"pattern": "C:/Windows/System32/config/systemprofile/AppData/Local/Jenkins/.jenkins/workspace/JenkinsDemo/Output.zip",
            }
        }
        stage ('Download') {
            steps {
                rtDownload(
                   serverId: "artifactory1234",
                    spec: '''{
                        "files": [
                            {
                             "pattern": "demo2/*.zip",
                             "target": "demo2/"
                            }
                        ]
                    }'''
                )
            }
        }
     }
 }
