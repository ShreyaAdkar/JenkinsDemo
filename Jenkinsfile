
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
                
                   serverId: "artifactory1234",
                    spec: '''{
                        "files": [
                            {
                             "pattern": "https://github.com/ShreyaAdkar/JenkinsDemo/Output.zip",
                             "target": "demo2/"
                            }
                        ]
                    }'''
                )
            }
        }
     }
 }
